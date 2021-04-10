---
title: Bereitstellen von fensterlosen Bearbeitungs Steuerelementen mit Fenster Funktionen
description: Die Fenster Funktionalität umfasst die Möglichkeit, Nachrichten zu empfangen, und den Besitz eines Geräte Kontexts, in den gezeichnet werden soll. Fensterlose Rich Edit-Steuerelemente erhalten diese Funktionalität über ein paar von Schnittstellen itextservices und itexthost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103948527"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Bereitstellen von fensterlosen Bearbeitungs Steuerelementen mit Fenster Funktionen

Die Fenster Funktionalität umfasst die Möglichkeit, Nachrichten zu empfangen, und den Besitz eines Geräte Kontexts, in den gezeichnet werden soll. Fensterlose Rich Edit-Steuerelemente erhalten diese Funktionalität über ein paar von Schnittstellen: [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="establish-the-window-functionality"></a>Einrichten der Fenster Funktionalität

Im folgenden Beispielcode wird veranschaulicht, wie der texthost und die Text Dienste erstellt werden.


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a>Bemerkungen

Der *hthchechedit* -Parameter im Codebeispiel ist ein Handle für das Msftedit.dll Modul, und es wird davon ausgegangen, dass dieses Handle bereits durch einen Aufrufen der **GetModuleHandle** -Funktion abgerufen wurde.

## <a name="complete-example"></a>Vollständiges Beispiel

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von fensterlosen Rich-Edit-Steuerelementen](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




