---
title: Bereitstellen von fensterlosen Rich Edit-Steuerelementen mit Fensterfunktionen
description: Die Fensterfunktion umfasst die Fähigkeit, Nachrichten zu empfangen, und den Besitz eines Gerätekontexts, in den gelost werden soll. Fensterlose Rich Edit-Steuerelemente erhalten diese Funktionalität über ein Paar von Schnittstellen ITextServices und ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce68a9e4e186be79e8f62cb009748916725e4af4f67d6522ed5eb47a92f33fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698600"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a>Bereitstellen von fensterlosen Rich Edit-Steuerelementen mit Fensterfunktionen

Die Fensterfunktion umfasst die Fähigkeit, Nachrichten zu empfangen, und den Besitz eines Gerätekontexts, in den gelost werden soll. Fensterlose Rich-Edit-Steuerelemente erhalten diese Funktionalität über ein Schnittstellenpaar: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und [**ITextHost.**](/windows/desktop/api/Textserv/nl-textserv-itexthost)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="establish-the-window-functionality"></a>Einrichten der Fensterfunktionalität

Der folgende Beispielcode veranschaulicht das Erstellen des Texthosts und der Textdienste.


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



## <a name="remarks"></a>Hinweise

Der *hmodRichEdit-Parameter* im Codebeispiel ist ein Handle für das Msftedit.dll-Modul, und es wird davon ausgegangen, dass dieses Handle bereits durch einen Aufruf der **GetModuleHandle-Funktion abgerufen** wurde.

## <a name="complete-example"></a>Vollständiges Beispiel

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Fensterlosen Rich Edit-Steuerelementen](using-windowless-rich-edit-controls.md)
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




