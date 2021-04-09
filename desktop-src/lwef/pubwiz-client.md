---
title: Client-Side Design
description: Skripts in serverseitigen HTML-Seiten kommunizieren mit dem Online-druckstellungs-Assistenten, in dem Sie gehostet werden. Diese Kommunikation erfolgt über Methoden und Eigenschaften, auf die das Window. extern-Objekt zugreift.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- Veröffentlichungs-Assistenten, Client seitiger Entwurf
- Window. extern, Veröffentlichungs-Assistenten
- Veröffentlichungs-Assistenten, Window. extern
- Veröffentlichungs-Assistenten, Entwurfs Überlegungen
- Veröffentlichungs-Assistenten, Assistent für Online-Druck Bestellungen
- Online-druckstellungs-Assistent, Client seitiger Entwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948717"
---
# <a name="client-side-design"></a>Client-Side Design

Skripts in serverseitigen HTML-Seiten kommunizieren mit dem Online-druckstellungs-Assistenten, in dem Sie gehostet werden. Diese Kommunikation erfolgt über Methoden und Eigenschaften, auf die das **Window. extern** -Objekt zugreift.

In diesem Dokument werden die folgenden Themen behandelt.

-   [Methoden und Eigenschaften](#methods-and-properties)
-   [Entwurfsaspekte](#design-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="methods-and-properties"></a>Methoden und Eigenschaften

Die folgenden Methoden und Eigenschaften sind über das **Window. extern** -Objekt verfügbar.

-   [**Finalback**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**Finalnext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Abbrechen**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**Passport Authenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**"Abadertext"**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**""-Schaltflächen**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Eigenschaft**](/windows/desktop/shell/iwebwizardhost-property)

Das Skript der serverseitigen Seite ruft diese Methoden auf, um den Client über Ereignisse während der Veröffentlichungs Prozedur zu benachrichtigen. Betrachten wir als Beispiel den [**finalback**](/windows/desktop/shell/iwebwizardhost-finalback) . Wenn der Assistent die erste serverseitige HTML-Seite anzeigt, ist er so bewaffnet, dass er die Handles für die Seiten des Assistenten vor und nach den gehosteten HTML-Seiten kennt. An diesem Punkt in unserem Beispiel klickt der Benutzer, der sich auf der ersten HTML-Seite befindet, auf die Schaltfläche " **zurück** ". Der Assistent sendet eine Benachrichtigung dieses Ereignisses an den Server. Beim Empfang dieser Nachricht bezieht sich das serverseitige Skript auf seinen **onback** -Handler für dieses Ereignis, das, da dies die erste HTML-Seite ist, die **Final Back** -Methode aufruft. Dadurch wechselt der Assistent zur Seite des Assistenten, der vor der Eingabe der serverseitigen Benutzeroberfläche angezeigt wird.

Eine ausführliche Erläuterung dieser Methoden und Eigenschaften finden Sie in der Dokumentation zu den Objekten [**webwizardhost**](/windows/desktop/shell/webwizardhost) und [**newwdevents**](/windows/desktop/shell/newwdevents) .

## <a name="design-considerations"></a>Entwurfsaspekte

Der HTML-Code für jede serverseitige Seite wird normalerweise im Assistenten Bereich angezeigt. Beachten Sie beim Entwerfen dieser Seiten, dass die Größe eines Assistenten Fensters nicht geändert werden kann. Daher sollten Seiten so erstellt und vergrößert werden, dass Scrollleisten nach Möglichkeit vermieden werden, um dem Benutzer eine reibungslose Navigation durch den Assistenten zu ermöglichen.

Jede HTML-Seite muss auch einen Handler für **onback**-, **OnNext**-und **OnCancel** -Ereignisse bereitstellen. Der **OnNext** -Handler behandelt außerdem das **Abschluss** Ereignis. Eine Seite, die keine **onback** -Funktion implementiert, wird als ungültig betrachtet und bewirkt, dass eine Fehlerseite angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Webwizardhost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**Newwentvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Server seitiges Design](pubwiz-server.md)
</dt> </dl>

 

 