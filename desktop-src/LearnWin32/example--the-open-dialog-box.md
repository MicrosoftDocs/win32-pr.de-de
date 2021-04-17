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
# <a name="example-the-open-dialog-box"></a>Beispiel: das Dialog Feld "Öffnen"

Das `Shapes` Beispiel, das wir verwendet haben, ist etwas verwirrend. Wir verwenden ein COM-Objekt, das Sie möglicherweise in einem echten Windows-Programm verwenden: das Dialogfeld " **Öffnen** ".

![Screenshot mit dem Dialogfeld "Öffnen"](images/fileopen01.png)

Um das Dialogfeld **Öffnen** anzuzeigen, kann ein Programm ein COM-Objekt verwenden, das als Common Item Dialog-Objekt bezeichnet wird. Das allgemeine Element Dialogfeld implementiert eine Schnittstelle mit dem Namen [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), die in der Header Datei "shobjidl. h" deklariert wird.

Hier ist ein Programm, das das Dialogfeld **Öffnen** für den Benutzer anzeigt. Wenn der Benutzer eine Datei auswählt, zeigt das Programm ein Dialogfeld an, das den Dateinamen enthält.


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



In diesem Code werden einige Konzepte verwendet, die weiter unten im Modul beschrieben werden. machen Sie sich also keine Sorgen, wenn Sie hier nicht alles verstehen. Im folgenden finden Sie eine grundlegende Übersicht über den Code:

1.  [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um die com-Bibliothek zu initialisieren.
2.  Rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um das allgemeine Element-Dialog Objekt zu erstellen und einen Zeiger auf die [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Schnittstelle des Objekts abzurufen.
3.  Die **Show** -Methode des Objekts, das das Dialogfeld für den Benutzer anzeigt, wird aufgerufen. Diese Methode wird blockiert, bis der Benutzer das Dialogfeld schließt.
4.  Ruft die [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) -Methode des Objekts auf. Diese Methode gibt einen Zeiger auf ein zweites com-Objekt zurück, das als *shellelementobjekt* bezeichnet wird. Das shellelement, das die [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -Schnittstelle implementiert, stellt die Datei dar, die der Benutzer ausgewählt hat.
5.  Aufrufen der [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) -Methode des shellelements. Diese Methode ruft den Dateipfad in Form einer Zeichenfolge ab.
6.  Zeigt ein Meldungs Feld an, das den Dateipfad anzeigt.
7.  Wenden [**Sie die Initialisierung der**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) com-Bibliothek an.

In den Schritten 1, 2 und 7 werden Funktionen aufgerufen, die von der com-Bibliothek definiert werden. Dabei handelt es sich um generische com-Funktionen. Schritte 3 – 5 Aufrufmethoden, die durch das Common Item Dialog-Objekt definiert werden.

Dieses Beispiel zeigt beide Arten der Objekt Erstellung: die generische [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion und eine Methode ([**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult)), die für das Common Item Dialog-Objekt spezifisch ist.

## <a name="next"></a>Nächste

[Verwalten der Lebensdauer eines Objekts](managing-the-lifetime-of-an-object.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dialog Feld Öffnen (Beispiel)](open-dialog-box-sample.md)
</dt> </dl>

 

 