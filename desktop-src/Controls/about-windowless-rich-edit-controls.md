---
title: Informationen zu fensterlosen Rich Edit-Steuerelementen
description: Ein fensterloses Rich Edit-Steuerelement, auch als Textdienstobjekt bezeichnet, ist ein Objekt, das die Funktionalität eines rich-Bearbeitungssteuerfelds ohne Angabe des Fensters bietet.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b68a2bc0317a884f0516b73b3674d104c4fa6c12f16bdc24960d7ea0ef8bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922180"
---
# <a name="about-windowless-rich-edit-controls"></a>Informationen zu fensterlosen Rich Edit-Steuerelementen

Ein fensterloses Rich Edit-Steuerelement, auch als Textdienstobjekt bezeichnet, ist [](rich-edit-controls.md) ein Objekt, das die Funktionalität eines rich-Bearbeitungssteuerfelds ohne Angabe des Fensters bietet. Zum Bereitstellen der Funktionalität eines Fensters, z. B. der Möglichkeit zum Empfangen von Nachrichten und eines Gerätekontexts, in den es zeichnen kann, verwenden fensterlose rich edit-Steuerelemente ein Paar von Schnittstellen: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Um ein fensterloses Rich Edit-Steuerelement zu erstellen, rufen Sie die [**CreateTextServices-Funktion**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) mit einem Zeiger auf Ihre Implementierung der [**ITextHost-Schnittstelle**](/windows/desktop/api/Textserv/nl-textserv-itexthost) auf. **CreateTextServices gibt** einen [**IUnknown-Zeiger**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) zurück, den Sie abfragen können, um einen Zeiger auf die [**ITextServices-Implementierung**](/windows/desktop/api/Textserv/nl-textserv-itextservices) des fensterlosen Steuerelements abzurufen.

Msftedit.dll exportiert einen Schnittstellenbezeichner **(IID) namens IID \_ ITextServices,** den Sie zum Abfragen des [**IUnknown-Zeigers**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) für die [**ITextServices-Schnittstelle verwenden**](/windows/desktop/api/Textserv/nl-textserv-itextservices) können. Das folgende Beispiel zeigt, wie **IID \_ ITextServices abgerufen** und zum Abrufen der **ITextServices-Schnittstelle verwendet** wird.


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



Msftedit.dll exportiert auch einen Schnittstellenbezeichner (IID) namens **IID \_ ITextHost,** der auf ähnliche Weise verwendet werden kann, um die [**ITextHost-Schnittstelle abfragen zu**](/windows/desktop/api/Textserv/nl-textserv-itexthost) können.

Die [**ITextHost-Schnittstelle**](/windows/desktop/api/Textserv/nl-textserv-itexthost) verfügt über Methoden, die das fensterlose Steuerelement aufruft, um Informationen zu Ihrem Fenster abzurufen. Beispielsweise ruft das Textdienstobjekt die [**TxGetDC-Methode**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) auf, um einen Gerätekontext abzurufen, in den es zeichnen kann. Das fensterlose Steuerelement ruft die [**TxNotify-Methode**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) auf, um Benachrichtigungen wie die Rich Edit-Benachrichtigungsmeldungen an den Texthost zu senden. Das Textdienstobjekt ruft andere **ITextHost-Methoden** auf, um den Texthost anweisen, andere fensterbezogene Dienste durchzuführen. Beispielsweise fordert die [**TxInvalidateRect-Methode**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) den Texthost auf, dem Updatebereich des Fensters ein Rechteck hinzuzufügen.

Ein standardmäßiges Rich-Edit-Steuerelement verfügt über eine Fensterprozedur, die Systemmeldungen und Nachrichten aus Ihrer Anwendung verarbeitet. Sie können das Fensterhand handle des Steuerelements verwenden, um ihm Nachrichten zum Ausführen von Textbearbeitung und anderen Vorgängen zu senden. Ein fensterloses Rich-Edit-Steuerelement verfügt jedoch über keine Fensterprozedur zum Empfangen und Verarbeiten von Nachrichten. Stattdessen stellt sie eine [**ITextServices-Schnittstelle**](/windows/desktop/api/Textserv/nl-textserv-itextservices) bereit. Um Nachrichten an ein fensterloses Rich Edit-Steuerelement zu senden, rufen Sie die [**TxSendMessage-Methode**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) auf. Sie können diese Methode verwenden, um umfangreiche Bearbeitungsnachrichten zu senden oder andere Nachrichten zu übergeben, die sich auf das Steuerelement auswirken, z. B. Systemmeldungen für Maus- oder Tastatureingaben.

Sie können das Textdienstobjekt auch als Teil eines [COM-aggregierten Objekts erstellen.](/windows/desktop/com/aggregation) Dies erleichtert das Aggregieren des Textdienstobjekts mit einem fensterlosen Component Object Model (COM)-Objekt.

 

 