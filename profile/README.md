
# LINK UTILI - da aggiornare ed organizzare :billed_cap:

## Indice
1. [Tools](#tools)
2. [C#](#c-sharp)
3. [Angular](#angular)
4. [Windows Forms e WPF](#wpf)
5. Varie Design
    - [Design Patterns](#design-patterns)
    - [DDD](#ddd)
7. [SOLID](#solid)
8. [GRASP](#grasp)
9. Codice
    - [Windows Form](#windows-form)
    - [MVVM](#mvvm)

Todo:
- [X] Inserire tabelle con definizioni SOLID e GRASP
- [ ] Abbellire e formattare tabelle SOLID e GRASP
- [ ] Sostituire quando possibile i link con versioni in italiano?

Legenda:
|Simbolo         |Significato             |
|:--------------:|------------------------|
| :cherries:     |Link fornito da noi     |
| :teacher:      |Link fornito dal docente|
| :it: :uk:      | Lingua (:uk: = default)|

[Come aggiungo emoji?](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)


## Tools <a name="tools"></a> <sub>[^](#indice)</sub>

[:teacher: yED - creazione diagrammi](https://www.yworks.com/products/yed/download)


## C# <a name="c-sharp"></a> <sub>[^](#indice)</sub>

[:teacher: C# coding convention](https://learn.microsoft.com/en-US/dotnet/csharp/fundamentals/coding-style/coding-conventions)


## Angular <a name="angular"></a> <sub>[^](#indice)</sub>

[:cherries::it: Slide introduzione angular](https://www.slideshare.net/valix85/introduzione-ad-angular-78)


## Windows Forms e WPF <a name="wpf"></a> <sub>[^](#indice)</sub>

[:teacher: Model-view-controller (wiki)](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)

[:teacher: Model–view–presenter (wiki)](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter#:~:text=MVP%20is%20a%20user%20interface,upon%20in%20the%20user%20interface)

[:teacher: :it: Procedura: creare un elemento Grid - WPF .NET Framework](https://learn.microsoft.com/it-it/dotnet/desktop/wpf/controls/how-to-create-a-grid-element?view=netframeworkdesktop-4.8)

[:teacher: Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)

[:teacher: Model–view–viewmodel (wiki)](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel)

[:teacher: Simple MVVM Pattern in WPF](https://www.c-sharpcorner.com/UploadFile/raj1979/simple-mvvm-pattern-in-wpf/)

## Roba Design

### Design Patterns <a name="design-patterns"></a> <sub>[^](#indice)</sub>
[:teacher: Design patterns wiki](https://en.wikipedia.org/wiki/Design_Patterns)

[:cherries: Design Patterns, Bad smells and Refractoring](https://refactoring.guru/)

[:cherries: Design Patterns with examples](https://medium.com/cp-massive-programming/design-patterns-cheat-sheet-list-e9a55d82de5d)

#### Quelli fatti: 
- [:teacher: Command pattern](https://en.wikipedia.org/wiki/Command_pattern)

- [:teacher: Facade pattern](https://en.wikipedia.org/wiki/Facade_pattern)

- [:teacher: Proxy pattern](https://en.wikipedia.org/wiki/Proxy_pattern)

- [:teacher: Chain-of-responsibility pattern](https://en.wikipedia.org/wiki/Chain-of-responsibility_pattern)

### DDD - Domain Driven Design <a name="ddd"></a> <sub>[^](#indice)</sub>
https://en.wikipedia.org/wiki/Domain-driven_design


## S.O.L.I.D. <a name="solid"></a> <sub>[^](#indice)</sub>

| | Princìpi | Definizione |
|-|----------|-------------|
|S|Single Responsibility|Una classe dovrebbe avere uno ed unico motivo per cambiare|
|O|Open-Closed          |Una qualsiasi entità software (classe, modulo,  funzione, ecc.) dovrebbe avere meccanismi che permettono di estenderne il comportamento senza apportare modifiche al codice preesistente. Quindi Aperte alle estensioni ma chiuse alle modifiche; da qui il nome Open-Closed.|
|L|Liskov Substitution  |Le classi derivate devono sempre poter essere sostituite dalle classi da cui queste derivano (superclassi) in maniera trasparente.|
|I|Interface Segregation Principle|Una classe client non dovrebbe dipendere da metodi che non usa, e che pertanto è preferibile che le interfacce siano molte, specifiche e piccole (composte da pochi metodi) piuttosto che poche, generali e grandi.|
|D|Dependency Inversion Principle|Una classe dovrebbe dipendere da astrazioni e non da concrete e specifiche implementazioni.|

[:teacher: SOLID](https://en.wikipedia.org/wiki/SOLID)

[:cherries::it: Spiegazione SOLID ](http://losviluppatore.it/solid-design-principles/)


## G.R.A.S.P. <a name="grasp"></a> <sub>[^](#indice)</sub>

|Pattern             | Problema | Soluzione |
|--------------------|----------|-----------|
|Information Expert  | Nella progettazione qual è il principio da seguire per assegnare una responsabilità ad una classe? | Si assegni la responsabilità alla classe che ha l’informazione necessaria per assumersi tale responsabilità |
|Creator             | Chi dovrebbe creare un’istanza di A? | Si assegni alla classe B la responsabilità di creare un’istanza della classe A se è vera una o più tra queste condizioni:<br> 1. B contiene o aggrega oggetti A (in una collezione)<br> 2. B registra oggetti A<br> 3. B usa oggetti A<br> 4. B ha i dati per inizializzare oggetti A|
|Controller          | A chi si assegna la responsabilità di gestire gli eventi esterni che entrano in una interfaccia utente? | La responsabilità di ricevere o gestire dall’esterno un evento che attiva un sistema si può assegnare:<br>– Mediante un unico rappresentante del sistema (façade pattern, non ancora visto)<br>– Mediante un controllore di sessione: per ogni caso d’uso il pattern definisce il primo oggetto che riceve e coordina un’operazione di sistema|
|Low Coupling (Disaccoppiamento)| Come ridurre le conseguenze delle modifiche ed incoraggiare il riuso? | Assegnare la responsabilità in modo che l’accoppiamento (dipendenze tra le classi) rimanga basso|
|High Cohesion       | come si disegnano classi coese e maneggevoli? | assegnare le responsabilità in modo da favorire la coesione |
|Polymorphism        |come gestire responsabilità alternative basate sul tipo (classe) | quando le alternative (o i comportamenti) variano col tipo (classe) assegna la responsabilità ai tipi per il quale il comportamento varia, usando operazioni polimorfe|
|Pure Fabrication    | quando usando Information Expert si violano Cohesion e/o Coupling, come assegnare le responsabilità?| introdurre una classe artificiosa (di convenienza) altamente coesa e poco accoppiata|
|Indirection         | dove assegnare una responsabilità, evitando l’accoppiamento diretto? Come disaccoppiare?| Assegna la responsabilità ad un oggetto intermediario, che dunque crea una indirezione tra gli altri componenti|
|Protected Variations| come progettare un oggetto le cui responsabilità non sono ancora fissate, senza che ci sia un impatto indesiderato su altri oggetti?| identifica i punti in cui sono prevedibili variazioni, e crea attorno ad essi un’interfaccia stabile Nota: è uno dei pattern più importanti nella progettazione software, generalizza la “Legge di Demetra”[^1]|

[:cherries::ita: Slide GRASP con spiegazioni ed esempi](https://www.cs.unibo.it/~cianca/wwwpages/ids/9.pdf)

[:teacher: GRASP (object-oriented design)](https://en.wikipedia.org/wiki/GRASP_(object-oriented_design))


# Codice <a name="codice"></a>

### Windows Form <a name="windows-form"></a> <sub>[^](#indice)</sub>

```C#
using System.Globalization;

namespace WinFormsApp2
{
    public partial class Form1 : Form
    {
        private decimal? _previousValue = 0;
        private decimal _currentValue = 0;
        private Operator _currentOperator;
        private Operator? _previousOperator = null;

        public Form1() : base()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
        }

        #region Business logics

        private void HandleNumberInput(decimal value)
        {
            myTextBox.Text += value.ToString(CultureInfo.InvariantCulture);
        }

        private void HandleOperator(Operator op)
        {
            if (string.IsNullOrWhiteSpace(myTextBox.Text))
            {
                if (string.IsNullOrWhiteSpace(resultTextBox.Text))
                {
                    MessageBox.Show("Please specify a value");
                    return;
                }
                else
                {
                    myTextBox.Text = resultTextBox.Text;
                }  
            }
           
            _currentValue = decimal.Parse(myTextBox.Text, CultureInfo.InvariantCulture);
            myTextBox.Text = string.Empty;
            _currentOperator = op;

            ComputePendingOperation();          
        }

        private void ComputePendingOperation()
        {
            if (_previousOperator != null && _previousValue != null)
            {
                decimal result;
                switch (_previousOperator)
                {
                    case Operator.Sum:
                        result = ((decimal)_previousValue) + _currentValue;
                        break;

                    case Operator.Difference:
                        result = ((decimal)_previousValue) - _currentValue;
                        break;

                    case Operator.Multiplication:
                        result = ((decimal)_previousValue) * _currentValue;
                        break;

                    case Operator.Division:
                        result = ((decimal)_previousValue) / _currentValue;
                        break;

                    default:
                        throw new InvalidOperationException("Unsupported operator: " + _previousOperator);
                }

                resultTextBox.Text = result.ToString(CultureInfo.InvariantCulture);
                _previousValue = result;
            }
            else
            {
                resultTextBox.Text = _currentValue.ToString(CultureInfo.InvariantCulture);
                _previousValue = (decimal)_currentValue;
            }

            _previousOperator = _currentOperator;
        }

        #endregion

        #region Events for numbers

        private void button1_Click(object sender, EventArgs e)
        {
            HandleNumberInput(1);
        }

        private void button2_Click(object sender, EventArgs e)
        {
            HandleNumberInput(2);
        }

        private void numberButton_Click(object sender, EventArgs e)
        {
            HandleNumberInput(3);
        }

        private void number4Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(4);
        }

        private void number5Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(5);
        }

        private void number6Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(6);
        }

        private void number7Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(7);
        }

        private void number8Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(8);
        }

        private void number9Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(9);
        }

        private void number0Button_Click(object sender, EventArgs e)
        {
            HandleNumberInput(0);
        }

        #endregion

        #region Events for operators

        private void sumButton_Click(object sender, EventArgs e)
        {
            HandleOperator(Operator.Sum);
        }

        private void differenceButton_Click(object sender, EventArgs e)
        {
            HandleOperator(Operator.Difference);
        }

        private void multiplicationButton_Click(object sender, EventArgs e)
        {
            HandleOperator(Operator.Multiplication);
        }

        private void divisionButton_Click(object sender, EventArgs e)
        {
            HandleOperator(Operator.Division);
        }

        private void equalsButton_Click(object sender, EventArgs e)
        {
            _currentValue = decimal.Parse(myTextBox.Text, CultureInfo.InvariantCulture);
            myTextBox.Text = string.Empty;
            ComputePendingOperation();
            _previousOperator = null;
            _previousValue = null;
            _currentOperator = Operator.Sum;
            _currentValue = 0;
        }

        #endregion
    }
}
```

## MVVM <a name="mvvm"></a> <sub>[^](#indice)</sub>

![MVVM](https://user-images.githubusercontent.com/93521016/195328034-19aaa601-ad9f-4821-a71e-a10b13aed1dd.jpg)

```C#
public partial class MainWindow : Window
    {
        private MyController _controller;
        private MyViewModel _viewModel;
        
        public MainWindow()
        {
            InitializeComponent();
            _viewModel = new MyViewModel();
            _controller = new MyController(_viewModel);
            DataContext = _viewModel;
        }
        
        private void Button_Click(object sender, RoutedEventArgs e)
        {
            _controller.DoSomething();
        }
    }
    
    public class MyController
    {
        private readonly MyViewModel _vm;
        
        public MyController(MyViewModel vm)
        {
            _vm = vm;
        }
        
        public void DoSomething()
        {
            _vm.Name = _vm.Prefix + DateTime.Now;
        }
    }
    
    public class MyViewModel : INotifyPropertyChanged
    {
        private string _name;
        
        public string Name
        {
            get => _name;
            set
            {
                _name = value;
                var pc = PropertyChanged;
                if (pc != null)
                pc(this, new PropertyChangedEventArgs(nameof(Name)));
            }
        }
        
        private string _prefix = "PREFIX";
        
        public string Prefix
        {
            get => _prefix;
            set
            {
                _prefix = value;
                var pc = PropertyChanged;
                if (pc != null)
                pc(this, new PropertyChangedEventArgs(nameof(Prefix)));
            }
        }
        
        public event PropertyChangedEventHandler? PropertyChanged;
    }
    
3:24
<TextBox Grid.Row="0" x:Name="MyTb" Text="{Binding Path=Name}"></TextBox>
<TextBox  Grid.Row="1" x:Name="MyPrefixTb" Text="{Binding Path=Prefix}"></TextBox>
<Button Grid.Row="2" Click="Button_Click">Do something</Button>
```       



[^1]:Principio Legge di Demetra
La “Legge di Demetra” (o “Non parlare agli
sconosciuti”) è un principio di progettazione che
suggerisce di disaccoppiare le classi:
-Ciascuna classe deve avere la minima
informazione necessaria sulle altre classi (incluse
le sue classi componenti)
-Ogni classe parla solo con le classi amiche (non
parla con le classi “sconosciute”)
