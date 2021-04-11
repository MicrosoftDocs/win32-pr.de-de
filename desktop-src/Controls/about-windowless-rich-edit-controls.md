---
title: Informationen zu fensterlosen Bearbeitungs Steuerelementen
description: Ein fensterloses Rich Edit-Steuerelement, das auch als Text Dienste-Objekt bezeichnet wird, ist ein Objekt, das die Funktionalität eines Rich-Edit-Steuer Elements bereitstellt, ohne das Fenster bereitzustellen.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949135"
---
# <a name="about-windowless-rich-edit-controls"></a>Informationen zu fensterlosen Bearbeitungs Steuerelementen

Ein fensterloses Rich Edit-Steuerelement, das auch als Text Dienste-Objekt bezeichnet wird, ist ein Objekt, das die Funktionalität eines [Rich-Edit-Steuer](rich-edit-controls.md) Elements bereitstellt, ohne das Fenster bereitzustellen. Um die Funktionalität eines Fensters bereitzustellen, z. b. die Fähigkeit, Nachrichten zu empfangen, und einen Gerätekontext, in dem Sie gezeichnet werden kann, verwenden fensterlose Rich Edit-Steuerelemente ein Schnittstellen Paar: [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).

Um ein fensterloses Bearbeitungs Steuerelement zu erstellen, rufen Sie [**die Funktion "**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) -Funktion" mit einem Zeiger auf die Implementierung der [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle auf. " **Kreatetextservices** " gibt einen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger zurück, den Sie Abfragen können, um einen Zeiger auf die [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) -Implementierung des fensterlosen Steuer Elements abzurufen.

Msftedit.dll exportiert eine Schnittstellen-ID (IID) namens **IID \_ itextservices** , die Sie verwenden können, um den [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger für die [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) -Schnittstelle abzufragen. Im folgenden Beispiel wird gezeigt, wie **IID \_ itextservices** abgerufen und zum Abrufen der **itextservices** -Schnittstelle verwendet wird.


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



Msftedit.dll exportiert außerdem eine Schnittstellen-ID (IID) namens **IID \_ itexthost** , die auf ähnliche Weise verwendet werden kann, um die [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle abzufragen.

Die [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle verfügt über Methoden, die vom fensterlosen Steuerelement aufgerufen werden, um Informationen zu Ihrem Fenster abzurufen. Beispielsweise ruft das Text Services-Objekt die [**txgetdc**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) -Methode auf, um einen Gerätekontext abzurufen, in den er gezeichnet werden kann. Das fensterlose Steuerelement ruft die [**txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) -Methode auf, um Benachrichtigungen (z. b. die Rich-Edit-Benachrichtigungs Meldungen) an den texthost zu senden. Das Text Services-Objekt ruft andere **itexthost** -Methoden auf, um den texthost zum Ausführen anderer Fenster bezogener Dienste aufzufordern. Beispielsweise fordert die [**txinvalidatup**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) -Methode den texthost zum Hinzufügen eines Rechtecks zum Aktualisierungs Bereich des Fensters auf.

Ein Standardmäßiges Bearbeitungs Steuerelement verfügt über eine Fenster Prozedur, mit der Systemmeldungen und Nachrichten von der Anwendung verarbeitet werden. Sie können das Fenster Handle des Steuer Elements verwenden, um IT-Nachrichten zum Durchführen von Textbearbeitung und anderen Vorgängen zu senden. Ein fensterloses Steuerelement für die Bearbeitung von Fenstern hat jedoch keine Fenster Prozedur zum empfangen und Verarbeiten von Nachrichten. Stattdessen wird eine [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) -Schnittstelle bereitstellt. Zum Senden von Nachrichten an ein fensterloses Rich-Edit-Steuerelement wird die [**txsendmessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) -Methode aufgerufen. Mit dieser Methode können Sie jede der Rich Edit-Nachrichten senden oder andere Nachrichten übergeben, die sich auf das Steuerelement auswirken, z. b. Systemmeldungen für Maus-oder Tastatureingaben.

Sie können das Objekt "Text Dienste" auch als Teil eines [com-aggregierten Objekts](/windows/desktop/com/aggregation)erstellen. Dies vereinfacht das Aggregieren des Text Services-Objekts mit einem COM-Objekt (Windows less Component Object Model).

 

 