---
title: WinMain der Einstiegspunkt der Anwendung
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208887"
---
# <a name="winmain-the-application-entry-point"></a><span data-ttu-id="02103-103">WinMain: der Einstiegspunkt der Anwendung</span><span class="sxs-lookup"><span data-stu-id="02103-103">WinMain: The Application Entry Point</span></span>

<span data-ttu-id="02103-104">Jedes Windows-Programm enthält eine Einstiegspunkt Funktion, die entweder **WinMain** oder **wWinMain** heißt.</span><span class="sxs-lookup"><span data-stu-id="02103-104">Every Windows program includes an entry-point function that is named either **WinMain** or **wWinMain**.</span></span> <span data-ttu-id="02103-105">Hier ist die Signatur für **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="02103-105">Here is the signature for **wWinMain**.</span></span>


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



<span data-ttu-id="02103-106">Die vier Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="02103-106">The four parameters are:</span></span>

-   <span data-ttu-id="02103-107">*HINSTANCE* wird als "Handle für eine Instanz" oder "Handle für ein Modul" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="02103-107">*hInstance* is something called a "handle to an instance" or "handle to a module."</span></span> <span data-ttu-id="02103-108">Das Betriebssystem verwendet diesen Wert, um die ausführbare Datei (exe) zu identifizieren, wenn Sie in den Arbeitsspeicher geladen wird.</span><span class="sxs-lookup"><span data-stu-id="02103-108">The operating system uses this value to identify the executable (EXE) when it is loaded in memory.</span></span> <span data-ttu-id="02103-109">Der Instanzhandle ist für bestimmte Windows-Funktionen erforderlich, z. –. zum Laden von Symbolen oder Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="02103-109">The instance handle is needed for certain Windows functions—for example, to load icons or bitmaps.</span></span>
-   <span data-ttu-id="02103-110">*hPrevInstance* hat keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="02103-110">*hPrevInstance* has no meaning.</span></span> <span data-ttu-id="02103-111">Es wurde in 16-Bit-Fenstern verwendet, ist aber jetzt immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="02103-111">It was used in 16-bit Windows, but is now always zero.</span></span>
-   <span data-ttu-id="02103-112">*pCmdLine* enthält die Befehlszeilenargumente als Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="02103-112">*pCmdLine* contains the command-line arguments as a Unicode string.</span></span>
-   <span data-ttu-id="02103-113">*nCmdShow* ist ein Flag, das besagt, ob das Hauptanwendungsfenster minimiert, maximiert oder normal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="02103-113">*nCmdShow* is a flag that says whether the main application window will be minimized, maximized, or shown normally.</span></span>

<span data-ttu-id="02103-114">Die-Funktion gibt einen **int** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="02103-114">The function returns an **int** value.</span></span> <span data-ttu-id="02103-115">Der Rückgabewert wird vom Betriebssystem nicht verwendet, Sie können jedoch den Rückgabewert verwenden, um einen Statuscode an ein anderes Programm zu übermitteln, das Sie schreiben.</span><span class="sxs-lookup"><span data-stu-id="02103-115">The return value is not used by the operating system, but you can use the return value to convey a status code to some other program that you write.</span></span>

<span data-ttu-id="02103-116">**WinAPI** ist die Aufruf Konvention.</span><span class="sxs-lookup"><span data-stu-id="02103-116">**WINAPI** is the calling convention.</span></span> <span data-ttu-id="02103-117">Eine *Aufruf Konvention* definiert, wie eine Funktion Parameter vom Aufrufer empfängt.</span><span class="sxs-lookup"><span data-stu-id="02103-117">A *calling convention* defines how a function receives parameters from the caller.</span></span> <span data-ttu-id="02103-118">Beispielsweise wird die Reihenfolge definiert, in der die Parameter im Stapel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="02103-118">For example, it defines the order that parameters appear on the stack.</span></span> <span data-ttu-id="02103-119">Stellen Sie einfach sicher, dass Sie Ihre **wWinMain** -Funktion wie gezeigt deklarieren.</span><span class="sxs-lookup"><span data-stu-id="02103-119">Just make sure to declare your **wWinMain** function as shown.</span></span>

<span data-ttu-id="02103-120">Die **WinMain** -Funktion ist mit **wWinMain** identisch, mit dem Unterschied, dass die Befehlszeilenargumente als ANSI-Zeichenfolge übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="02103-120">The **WinMain** function is identical to **wWinMain**, except the command-line arguments are passed as an ANSI string.</span></span> <span data-ttu-id="02103-121">Die Unicode-Version wird bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="02103-121">The Unicode version is preferred.</span></span> <span data-ttu-id="02103-122">Sie können die ANSI- **WinMain** -Funktion auch dann verwenden, wenn Sie das Programm als Unicode kompilieren.</span><span class="sxs-lookup"><span data-stu-id="02103-122">You can use the ANSI **WinMain** function even if you compile your program as Unicode.</span></span> <span data-ttu-id="02103-123">Um eine Unicode-Kopie der Befehlszeilenargumente abzurufen, müssen Sie die [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02103-123">To get a Unicode copy of the command-line arguments, call the [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function.</span></span> <span data-ttu-id="02103-124">Diese Funktion gibt alle Argumente in einer einzelnen Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="02103-124">This function returns all of the arguments in a single string.</span></span> <span data-ttu-id="02103-125">Wenn die Argumente als Array im *argv*-Format angezeigt werden sollen, übergeben Sie diese Zeichenfolge an [**commandlineumargvw**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span><span class="sxs-lookup"><span data-stu-id="02103-125">If you want the arguments as an *argv*-style array, pass this string to [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).</span></span>

<span data-ttu-id="02103-126">Wie weiß der Compiler, dass **wWinMain** anstelle der Standard- **Main** -Funktion aufgerufen werden soll?</span><span class="sxs-lookup"><span data-stu-id="02103-126">How does the compiler know to invoke **wWinMain** instead of the standard **main** function?</span></span> <span data-ttu-id="02103-127">Tatsächlich ist zu tun, dass die Microsoft C-Lauf Zeit Bibliothek (CRT) eine Implementierung von **Main** bereitstellt, die entweder **WinMain** oder **wWinMain** aufruft.</span><span class="sxs-lookup"><span data-stu-id="02103-127">What actually happens is that the Microsoft C runtime library (CRT) provides an implementation of **main** that calls either **WinMain** or **wWinMain**.</span></span>

> [!Note]  
> <span data-ttu-id="02103-128">Die CRT führt einige zusätzliche Aufgaben in **Main** aus.</span><span class="sxs-lookup"><span data-stu-id="02103-128">The CRT does some additional work inside **main**.</span></span> <span data-ttu-id="02103-129">Beispielsweise werden alle statischen Initialisierer vor **wWinMain** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="02103-129">For example, any static initializers are called before **wWinMain**.</span></span> <span data-ttu-id="02103-130">Obwohl Sie den Linker anweisen können, eine andere Einstiegspunkt Funktion zu verwenden, verwenden Sie den Standardwert, wenn Sie mit der CRT verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="02103-130">Although you can tell the linker to use a different entry-point function, use the default if you link to the CRT.</span></span> <span data-ttu-id="02103-131">Andernfalls wird der CRT-Initialisierungs Code übersprungen, mit unvorhersehbaren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="02103-131">Otherwise, the CRT initialization code will be skipped, with unpredictable results.</span></span> <span data-ttu-id="02103-132">(Beispielsweise werden globale Objekte nicht ordnungsgemäß initialisiert.)</span><span class="sxs-lookup"><span data-stu-id="02103-132">(For example, global objects will not be initialized correctly.)</span></span>

 

<span data-ttu-id="02103-133">Hier ist eine leere **WinMain** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="02103-133">Here is an empty **WinMain** function.</span></span>


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



<span data-ttu-id="02103-134">Nachdem Sie nun über den Einstiegspunkt verfügen und einige grundlegende Terminologie und Codierungs Konventionen verstanden haben, sind Sie bereit, ein umfassendes Fensterprogramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02103-134">Now that you have the entry point and understand some of the basic terminology and coding conventions, you are ready to create a complete Window program.</span></span>

## <a name="next"></a><span data-ttu-id="02103-135">Nächste</span><span class="sxs-lookup"><span data-stu-id="02103-135">Next</span></span>

<span data-ttu-id="02103-136">[Modul 1. Ihr erstes Windows-Programm](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="02103-136">[Module 1. Your First Windows Program](your-first-windows-program.md).</span></span>

 

 