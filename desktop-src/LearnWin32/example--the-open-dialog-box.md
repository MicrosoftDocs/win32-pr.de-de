---
title: Beispiel für das Dialog Feld "Öffnen"
description: Das von uns verwendete Shapes-Beispiel ist etwas konstruiert. Wir verwenden ein COM-Objekt, das Sie möglicherweise in einem echten Windows-Programm öffnen, das geöffnet wird.
ms.assetid: f426cf83-ed24-4eeb-bc28-b5871b824525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d896c5928c5bcf5e7dae7835d011ddf0f1fbd6e6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390282"
---
# <a name="example-the-open-dialog-box"></a><span data-ttu-id="1b544-104">Beispiel: das Dialog Feld "Öffnen"</span><span class="sxs-lookup"><span data-stu-id="1b544-104">Example: The Open Dialog Box</span></span>

<span data-ttu-id="1b544-105">Das `Shapes` Beispiel, das wir verwendet haben, ist etwas verwirrend.</span><span class="sxs-lookup"><span data-stu-id="1b544-105">The `Shapes` example that we have been using is somewhat contrived.</span></span> <span data-ttu-id="1b544-106">Wir verwenden ein COM-Objekt, das Sie möglicherweise in einem echten Windows-Programm verwenden: das Dialogfeld " **Öffnen** ".</span><span class="sxs-lookup"><span data-stu-id="1b544-106">Let's turn to a COM object that you might use in a real Windows program: the **Open** dialog box.</span></span>

![Screenshot mit dem Dialogfeld "Öffnen"](images/fileopen01.png)

<span data-ttu-id="1b544-108">Um das Dialogfeld **Öffnen** anzuzeigen, kann ein Programm ein COM-Objekt verwenden, das als Common Item Dialog-Objekt bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1b544-108">To show the **Open** dialog box, a program can use a COM object called the Common Item Dialog object.</span></span> <span data-ttu-id="1b544-109">Das allgemeine Element Dialogfeld implementiert eine Schnittstelle mit dem Namen [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), die in der Header Datei "shobjidl. h" deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="1b544-109">The Common Item Dialog implements an interface named [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), which is declared in the header file Shobjidl.h.</span></span>

<span data-ttu-id="1b544-110">Hier ist ein Programm, das das Dialogfeld **Öffnen** für den Benutzer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1b544-110">Here is a program that displays the **Open** dialog box to the user.</span></span> <span data-ttu-id="1b544-111">Wenn der Benutzer eine Datei auswählt, zeigt das Programm ein Dialogfeld an, das den Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="1b544-111">If the user selects a file, the program shows a dialog box that contains the file name.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        IFileOpenDialog *pFileOpen;

        // Create the FileOpenDialog object.
        hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
                IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                IShellItem *pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBoxW(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                    pItem->Release();
                }
            }
            pFileOpen->Release();
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="1b544-112">In diesem Code werden einige Konzepte verwendet, die weiter unten im Modul beschrieben werden. machen Sie sich also keine Sorgen, wenn Sie hier nicht alles verstehen.</span><span class="sxs-lookup"><span data-stu-id="1b544-112">This code uses some concepts that will be described later in the module, so don't worry if you do not understand everything here.</span></span> <span data-ttu-id="1b544-113">Im folgenden finden Sie eine grundlegende Übersicht über den Code:</span><span class="sxs-lookup"><span data-stu-id="1b544-113">Here is a basic outline of the code:</span></span>

1.  <span data-ttu-id="1b544-114">[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um die com-Bibliothek zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="1b544-114">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="1b544-115">Rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um das allgemeine Element-Dialog Objekt zu erstellen und einen Zeiger auf die [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Schnittstelle des Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b544-115">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Common Item Dialog object and get a pointer to the object's [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span>
3.  <span data-ttu-id="1b544-116">Die **Show** -Methode des Objekts, das das Dialogfeld für den Benutzer anzeigt, wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1b544-116">Call the object's **Show** method, which shows the dialog box to the user.</span></span> <span data-ttu-id="1b544-117">Diese Methode wird blockiert, bis der Benutzer das Dialogfeld schließt.</span><span class="sxs-lookup"><span data-stu-id="1b544-117">This method blocks until the user dismisses the dialog box.</span></span>
4.  <span data-ttu-id="1b544-118">Ruft die [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) -Methode des Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="1b544-118">Call the object's [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method.</span></span> <span data-ttu-id="1b544-119">Diese Methode gibt einen Zeiger auf ein zweites com-Objekt zurück, das als *shellelementobjekt* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1b544-119">This method returns a pointer to a second COM object, called a *Shell item* object.</span></span> <span data-ttu-id="1b544-120">Das shellelement, das die [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -Schnittstelle implementiert, stellt die Datei dar, die der Benutzer ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="1b544-120">The Shell item, which implements the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, represents the file that the user selected.</span></span>
5.  <span data-ttu-id="1b544-121">Aufrufen der [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) -Methode des shellelements.</span><span class="sxs-lookup"><span data-stu-id="1b544-121">Call the Shell item's [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method.</span></span> <span data-ttu-id="1b544-122">Diese Methode ruft den Dateipfad in Form einer Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="1b544-122">This method gets the file path, in the form of a string.</span></span>
6.  <span data-ttu-id="1b544-123">Zeigt ein Meldungs Feld an, das den Dateipfad anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1b544-123">Show a message box that displays the file path.</span></span>
7.  <span data-ttu-id="1b544-124">Wenden [**Sie die Initialisierung der**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) com-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1b544-124">Call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize the COM library.</span></span>

<span data-ttu-id="1b544-125">In den Schritten 1, 2 und 7 werden Funktionen aufgerufen, die von der com-Bibliothek definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b544-125">Steps 1, 2, and 7 call functions that are defined by the COM library.</span></span> <span data-ttu-id="1b544-126">Dabei handelt es sich um generische com-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1b544-126">These are generic COM functions.</span></span> <span data-ttu-id="1b544-127">Schritte 3 – 5 Aufrufmethoden, die durch das Common Item Dialog-Objekt definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b544-127">Steps 3–5 call methods that are defined by the Common Item Dialog object.</span></span>

<span data-ttu-id="1b544-128">Dieses Beispiel zeigt beide Arten der Objekt Erstellung: die generische [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion und eine Methode ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)), die für das Common Item Dialog-Objekt spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="1b544-128">This example shows both varieties of object creation: The generic [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, and a method ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)) that is specific to the Common Item Dialog object.</span></span>

## <a name="next"></a><span data-ttu-id="1b544-129">Nächste</span><span class="sxs-lookup"><span data-stu-id="1b544-129">Next</span></span>

[<span data-ttu-id="1b544-130">Verwalten der Lebensdauer eines Objekts</span><span class="sxs-lookup"><span data-stu-id="1b544-130">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a><span data-ttu-id="1b544-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b544-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b544-132">Dialog Feld Öffnen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="1b544-132">Open Dialog Box Sample</span></span>](open-dialog-box-sample.md)
</dt> </dl>

 

 