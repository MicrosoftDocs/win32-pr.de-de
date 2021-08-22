---
title: Client-Side Design
description: Skripts auf serverseitigen HTML-Seiten kommunizieren mit dem Client des Onlinedruckreihenfolge-Assistenten, in dem es gehostet wird. Diese Kommunikation erfolgt über Methoden und Eigenschaften, auf die das window.external-Objekt zugreift.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- Veröffentlichungs-Assistenten, clientseitiger Entwurf
- window.external, Veröffentlichungs-Assistenten
- Veröffentlichungs-Assistenten,window.external
- Veröffentlichungs-Assistenten,Überlegungen zum Entwurf
- Veröffentlichungs-Assistenten,Onlinedruckreihenfolge-Assistent
- Onlinedruckreihenfolge-Assistent, clientseitiger Entwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40aafc7a08820125df222c1c6d911b0d2b4d0a1fb625b7c62fc6d4be8bebd7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665080"
---
# <a name="client-side-design"></a>Client-Side Design

Skripts auf serverseitigen HTML-Seiten kommunizieren mit dem Client des Onlinedruckreihenfolge-Assistenten, in dem es gehostet wird. Diese Kommunikation erfolgt über Methoden und Eigenschaften, auf die das **window.external-Objekt** zugreift.

Die folgenden Themen werden in diesem Dokument behandelt.

-   [Methoden und Eigenschaften](#methods-and-properties)
-   [Entwurfsaspekte](#design-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="methods-and-properties"></a>Methoden und Eigenschaften

Die folgenden Methoden und Eigenschaften sind über das **window.external-Objekt** verfügbar.

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Abbrechen**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Eigenschaft**](/windows/desktop/shell/iwebwizardhost-property)

Das Skript der serverseitigen Seite ruft diese Methoden auf, um den Client während des Veröffentlichungsvorgangs über Ereignisse zu benachrichtigen. Sehen wir uns [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) als Beispiel an. Wenn der Assistent die erste serverseitige HTML-Seite anzeigt, verfügt er über Kenntnisse über die Handles für die Assistentenseiten, die den gehosteten HTML-Seiten vorangehen und diesen folgen. An diesem Punkt in unserem Beispiel klickt der Benutzer auf dieser ersten HTML-Seite auf die Schaltfläche **Zurück.** Der Assistent sendet eine Benachrichtigung über dieses Ereignis an den Server. Beim Empfang dieser Nachricht verweist das serverseitige Skript auf seinen **OnBack-Handler** für dieses Ereignis, der die **FinalBack-Methode** aufruft, da dies die erste HTML-Seite ist. Dadurch navigiert der Assistent zur Seite des Assistenten, die angezeigt wird, bevor er die serverseitige Benutzeroberfläche betritt.

Eine vollständige Erläuterung dieser Methoden und Eigenschaften finden Sie in der Dokumentation für die Objekte [**WebWizardHost**](/windows/desktop/shell/webwizardhost) und [**NewWDEvents.**](/windows/desktop/shell/newwdevents)

## <a name="design-considerations"></a>Entwurfsaspekte

HTML-Code, aus dem jede serverseitige Seite besteht, wird normalerweise im Assistentenbereich angezeigt. Beachten Sie beim Entwerfen dieser Seiten, dass die Größe eines Assistentenfensters nicht geändert werden kann. Daher sollten Seiten so konstruiert und dimensioniert werden, dass Scrollleisten möglichst vermieden werden, um dem Benutzer eine reibungslose Navigation durch den Assistenten zu ermöglichen.

Jede HTML-Seite muss auch einen Handler für **OnBack-,** **OnNext-** und **OnCancel-Ereignisse** bereitstellen. Der **OnNext-Handler** behandelt auch das **Finish-Ereignis.** Eine Seite, die keine **OnBack-Funktion** implementiert, wird als ungültig betrachtet und bewirkt, dass eine Fehlerseite angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Serverseitiger Entwurf](pubwiz-server.md)
</dt> </dl>

 

 