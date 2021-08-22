---
title: Server-Side Design
description: Serverseitige Funktionen kommunizieren mit dem Client-Assistenten über das windows.external-Objekt. Serverseitige Skripts stellen diese Funktionen zum Reagieren auf Assistentenereignisse und zum Abrufen von Informationen über den Assistenten zur Verfügung.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- Veröffentlichungs-Assistenten,serverseitiger Entwurf
- window.external,Veröffentlichungs-Assistenten
- Veröffentlichungs-Assistenten,window.external
- Veröffentlichungs-Assistenten,Navigationsskriptfunktionen
- Skripts,Veröffentlichungs-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075e5a18b2150e504b6424fae2591ed83fdf707a6a20231b8f1186ddb6f3a67b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555810"
---
# <a name="server-side-design"></a>Server-Side Design

Serverseitige Funktionen kommunizieren mit dem Client-Assistenten über das **windows.external-Objekt.** Serverseitige Skripts stellen diese Funktionen zum Reagieren auf Assistentenereignisse und zum Abrufen von Informationen über den Assistenten zur Verfügung.

Die folgenden Themen werden in diesem Dokument behandelt.

-   [Implementieren von Navigationsskriptfunktionen](#implementing-navigation-script-functions)
    -   [OnBack()](#onback)
    -   [OnNext()](#onnext)
    -   [OnCancel()](#oncancel)
-   [Andere Methoden und Eigenschaften](#other-methods-and-properties)
    -   [Methoden](#methods)
    -   [Eigenschaften](#properties)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementieren von Navigationsskriptfunktionen

Serverseitiges Skript auf jeder HTML-Seite reagiert über Funktionen für **OnBack,** **OnNext** und **OnCancel auf Navigationsschaltflächen.** Auf diese Funktionen muss über **IHTMLDocument::get \_ Script** auf dem Client zugegriffen werden können, und es müssen keine Parameter verwendet werden.

### <a name="onback"></a>OnBack()

-   Antwortet, wenn der Benutzer im **Assistenten auf** Zurück klickt.
-   Wenn die aktuelle serverseitige Seite die erste serverseitige Seite ist, rufen Sie **window.external.FinalBack** auf, um den Client anweisen, zur vorherigen clientseitigen Seite zu navigieren.
-   Wenn die aktuelle serverseitige Seite nicht die erste serverseitige Seite ist, navigieren Sie zur vorherigen serverseitigen Seite.
-   Diese Funktion muss für jede Seite implementiert werden. Jede Seite, bei der dies nicht der Fall ist, wird als ungültig betrachtet und zeigt eine Fehlerseite an.

### <a name="onnext"></a>OnNext()

-   Antwortet, wenn der Benutzer im **Assistenten auf** Weiter klickt.
-   Wenn die aktuelle serverseitige Seite die letzte serverseitige Seite ist, rufen Sie **window.external.FinalNext** auf, um den Client anweisen, zur nächsten clientseitigen Seite zu navigieren oder den Assistenten abzuschließen.
-   Wenn die aktuelle serverseitige Seite nicht die letzte serverseitige Seite ist, navigieren Sie zur nächsten serverseitigen Seite.

### <a name="oncancel"></a>OnCancel()

-   Antwortet, wenn der Benutzer im **Assistenten auf** Abbrechen klickt.
-   Die Benutzeroberfläche sollte so entworfen werden, dass der Benutzer jederzeit abbrechen kann.
-   Sobald eine Verarbeitung in der **OnCancel-Funktion** verarbeitet wurde, schließt der Client den Assistenten.

## <a name="other-methods-and-properties"></a>Andere Methoden und Eigenschaften

Auf vom Client implementierte Funktionen wird über **windows.external zugegriffen,** ebenso wie auf Eigenschaften. Folgende Dienste sind verfügbar:

### <a name="methods"></a>Methoden

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Eigenschaften

-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Eigenschaft**](/windows/desktop/shell/iwebwizardhost-property)

Das folgende Codebeispiel zeigt serverseitigen Code für eine einfache Assistentenseite, die die Fehlerseite des Webdiensts implementiert.


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientseitiger Entwurf](pubwiz-client.md)
</dt> <dt>

[Registrieren eines Diensts](pubwiz-reg.md)
</dt> </dl>

 

 