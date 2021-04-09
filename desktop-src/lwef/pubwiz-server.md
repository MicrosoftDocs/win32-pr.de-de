---
title: Server-Side Design
description: Server seitige Funktionen kommunizieren über das Windows. externe-Objekt mit dem-Client-Assistenten. Server seitiges Skript stellt diese Funktionen bereit, um auf Assistenten Ereignisse zu reagieren und Informationen zum Assistenten abzurufen.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- Veröffentlichungs-Assistenten, serverseitiger Entwurf
- Window. extern, Veröffentlichungs-Assistenten
- Veröffentlichungs-Assistenten, Window. extern
- Veröffentlichungs-Assistenten, Navigations Skriptfunktionen
- Skripts, Veröffentlichungs-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948747"
---
# <a name="server-side-design"></a>Server-Side Design

Server seitige Funktionen kommunizieren über das **Windows. externe** -Objekt mit dem-Client-Assistenten. Server seitiges Skript stellt diese Funktionen bereit, um auf Assistenten Ereignisse zu reagieren und Informationen zum Assistenten abzurufen.

In diesem Dokument werden die folgenden Themen behandelt.

-   [Implementieren von Navigations Skriptfunktionen](#implementing-navigation-script-functions)
    -   [Onback ()](#onback)
    -   [OnNext ()](#onnext)
    -   [OnCancel ()](#oncancel)
-   [Andere Methoden und Eigenschaften](#other-methods-and-properties)
    -   [Methoden](#methods)
    -   [Eigenschaften](#properties)
-   [Zugehörige Themen](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implementieren von Navigations Skriptfunktionen

Server seitiges Skript in jeder HTML-Seite antwortet auf Navigations Schaltflächen durch Funktionen für **onback**, **OnNext** und **OnCancel**. Auf diese Funktionen muss über das **IHTMLDocument:: get- \_ Skript** auf dem Client zugegriffen werden können, und es müssen keine Parameter übernommen werden.

### <a name="onback"></a>Onback ()

-   Reagiert, wenn der Benutzer auf den Assistenten **zurück** klickt.
-   Wenn die aktuelle serverseitige Seite die erste serverseitige Seite ist, rufen Sie **Window. extern. finalback** auf, um den Client anzuweisen, zur vorherigen Client seitigen Seite zu navigieren.
-   Wenn die aktuelle serverseitige Seite nicht die erste serverseitige Seite ist, navigieren Sie zur vorherigen serverseitigen Seite.
-   Diese Funktion muss für jede Seite implementiert werden. Jede Seite, die nicht ausgeführt werden kann, wird als ungültig betrachtet und zeigt eine Fehlerseite an.

### <a name="onnext"></a>OnNext ()

-   Reagiert, wenn der Benutzer im Assistenten auf **weiter** klickt.
-   Wenn die aktuelle serverseitige Seite die letzte serverseitige Seite ist, rufen Sie **Window. extern. finalnext** auf, um den Client anzuweisen, zur nächsten Client seitigen Seite zu navigieren, oder um den Assistenten abzuschließen.
-   Wenn die aktuelle serverseitige Seite nicht die letzte serverseitige Seite ist, navigieren Sie zur nächsten serverseitigen Seite.

### <a name="oncancel"></a>OnCancel ()

-   Reagiert, wenn der Benutzer im Assistenten auf **Abbrechen** klickt.
-   Die Benutzeroberfläche sollte so entworfen werden, dass der Benutzer Sie jederzeit abbrechen kann.
-   Nachdem die Verarbeitung in der **OnCancel** -Funktion verarbeitet wurde, schließt der Client den Assistenten.

## <a name="other-methods-and-properties"></a>Andere Methoden und Eigenschaften

Der Zugriff auf Client implementierte Funktionen erfolgt über **Windows. extern**, ebenso wie Eigenschaften. Folgende Dienste stehen zur Verfügung:

### <a name="methods"></a>Methoden

-   [**"Abadertext"**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**""-Schaltflächen**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Passport Authenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Eigenschaften

-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Eigenschaft**](/windows/desktop/shell/iwebwizardhost-property)

Das folgende Codebeispiel zeigt serverseitigen Code für eine einfache Assistenten Seite, die die Fehlerseite des Webdiensts implementiert.


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

[Client seitiges Design](pubwiz-client.md)
</dt> <dt>

[Registrieren eines Dienstanbieter](pubwiz-reg.md)
</dt> </dl>

 

 