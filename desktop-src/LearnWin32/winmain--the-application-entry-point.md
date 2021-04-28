---
<span data-ttu-id="353ae-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="353ae-101">title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="353ae-102">WinMain: Der Einstiegspunkt für die Anwendung</span><span class="sxs-lookup"><span data-stu-id="353ae-102">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="353ae-103">Jedes Windows-Programm enthält eine Einstiegspunktfunktion mit dem Namen **WinMain** oder **wWinMain.**</span><span class="sxs-lookup"><span data-stu-id="353ae-103">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="353ae-104">Hier ist die Signatur für **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="353ae-104">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="353ae-105">Die vier Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="353ae-105">The four parameters are:</span></span>

-   <span data-ttu-id="353ae-106">*hInstance* wird als "Handle für eine Instanz" oder "Handle für ein Modul" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="353ae-106">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="353ae-107">Das Betriebssystem verwendet diesen Wert, um die ausführbare Datei (EXE) zu identifizieren, wenn sie in den Arbeitsspeicher geladen wird.</span><span class="sxs-lookup"><span data-stu-id="353ae-107">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="353ae-108">Das Instanzhandle wird für bestimmte Windows-Funktionen benötigt, z. B. zum Laden von Symbolen oder Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="353ae-108">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="353ae-109">*hPrevInstance* hat keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="353ae-109">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="353ae-110">Sie wurde in 16-Bit-Windows verwendet, ist jetzt aber immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="353ae-110">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="353ae-111">*pCmdLine* enthält die Befehlszeilenargumente als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="353ae-111">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="353ae-112">*nCmdShow* ist ein Flag, das angibt, ob das Hauptanwendungsfenster minimiert, maximiert oder normal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="353ae-112">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="353ae-113">Die Funktion gibt einen **int-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="353ae-113">The function returns an **int** value.</span></span> <span data-ttu-id="353ae-114">Der Rückgabewert wird nicht vom Betriebssystem verwendet, aber Sie können den Rückgabewert verwenden, um einen Statuscode an ein anderes Programm zu übermitteln, das Sie schreiben.</span><span class="sxs-lookup"><span data-stu-id="353ae-114">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="353ae-115">**WINAPI** ist die Aufrufkonvention.</span><span class="sxs-lookup"><span data-stu-id="353ae-115">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="353ae-116">Eine *Aufrufkonvention* definiert, wie eine Funktion Parameter vom Aufrufer empfängt.</span><span class="sxs-lookup"><span data-stu-id="353ae-116">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="353ae-117">Beispielsweise wird die Reihenfolge definiert, in der Parameter im Stapel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="353ae-117">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="353ae-118">Stellen Sie einfach sicher, dass Sie Ihre **wWinMain-Funktion** wie gezeigt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="353ae-118">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="353ae-119">Die **WinMain-Funktion** ist mit **wWinMain** identisch, mit der Ausnahme, dass die Befehlszeilenargumente als ANSI-Zeichenfolge übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="353ae-119">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="353ae-120">Die Unicode-Version wird bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="353ae-120">The Unicode version is preferred.</span></span> <span data-ttu-id="353ae-121">Sie können die ANSI **WinMain-Funktion** auch dann verwenden, wenn Sie Ihr Programm als Unicode kompilieren.</span><span class="sxs-lookup"><span data-stu-id="353ae-121">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="353ae-122">Um eine Unicode-Kopie der Befehlszeilenargumente zu erhalten, rufen Sie die [**GetCommandLine-Funktion**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) auf.</span><span class="sxs-lookup"><span data-stu-id="353ae-122">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="353ae-123">Diese Funktion gibt alle Argumente in einer einzelnen Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="353ae-123">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="353ae-124">Wenn Sie die Argumente als Array im *Argv-Stil* verwenden möchten, übergeben Sie diese Zeichenfolge an [**CommandLineToArgvW.**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw)</span><span class="sxs-lookup"><span data-stu-id="353ae-124">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="353ae-125">Woher weiß der Compiler, **dass wWinMain anstelle** der Standard-Main-Funktion **aufgerufen** werden soll?</span><span class="sxs-lookup"><span data-stu-id="353ae-125">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="353ae-126">Tatsächlich geschieht, dass die Microsoft C-Laufzeitbibliothek (CRT) eine Implementierung von **main** bietet, die **entweder WinMain** oder **wWinMain aufruft.**</span><span class="sxs-lookup"><span data-stu-id="353ae-126">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="353ae-127">Die CRT führt einige zusätzliche Arbeit in main **durch.**</span><span class="sxs-lookup"><span data-stu-id="353ae-127">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="353ae-128">Beispielsweise werden alle statischen Initialisierer vor **wWinMain aufgerufen.**</span><span class="sxs-lookup"><span data-stu-id="353ae-128">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="353ae-129">Obwohl Sie dem Linker mitteilen können, dass er eine andere Einstiegspunktfunktion verwendet, verwenden Sie die Standardfunktion, wenn Sie eine Verknüpfung mit der CRT verwenden.</span><span class="sxs-lookup"><span data-stu-id="353ae-129">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="353ae-130">Andernfalls wird der CRT-Initialisierungscode mit unvorhersehbaren Ergebnissen übersprungen.</span><span class="sxs-lookup"><span data-stu-id="353ae-130">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="353ae-131">(Globale Objekte werden beispielsweise nicht ordnungsgemäß initialisiert.)</span><span class="sxs-lookup"><span data-stu-id="353ae-131">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="353ae-132">Hier ist eine leere **WinMain-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="353ae-132">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="353ae-133">Nachdem Sie nun über den Einstiegspunkt verfügen und einige der grundlegenden Terminologie und Codierungskonventionen verstanden haben, können Sie ein vollständiges Window-Programm erstellen.</span><span class="sxs-lookup"><span data-stu-id="353ae-133">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="353ae-134">Nächste</span><span class="sxs-lookup"><span data-stu-id="353ae-134">Next</span></span>

<span data-ttu-id="353ae-135">[Modul 1. Ihr erstes Windows-Programm.](your-first-windows-program.md)</span><span class="sxs-lookup"><span data-stu-id="353ae-135">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 
