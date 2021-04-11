---
title: Registrieren eines gehosteten Geräts beim Geräte Host
description: Das Registrieren eines gehosteten Geräts bedeutet, dass der Geräte Host die Geräte Beschreibung und das zugehörige Geräte Steuerungsobjekt bereitstellt.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a607af4f6ada359a9ee32e98e416d8271fd502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206681"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registrieren eines gehosteten Geräts beim Geräte Host

Das Registrieren eines gehosteten Geräts bedeutet, dass der Geräte Host die Geräte Beschreibung und das zugehörige Geräte Steuerungsobjekt bereitstellt. Der Geräte Host erstellt dann eine komplette UPnP-Geräte Beschreibung, veröffentlicht Sie und kündigt das Gerät mithilfe des UPnP-Ermittlungs Protokolls im Netzwerk an. Sobald ein Gerät veröffentlicht wurde, ist es für Steuerungs Punkte verfügbar.

Geräte werden auf zwei Arten registriert:

-   Eine Anwendung erstellt eine Instanz des Geräte Steuerungs Objekts und übergibt einen Zeiger darauf an den Geräte Host.
-   Die Anwendung übergibt die ProgID für ein registriertes Geräte Steuerungsobjekt an den Geräte Host. Der Geräte Host instanziiert ihn, wenn der Geräte Host die erste Anforderung für das Gerät empfängt.

Unabhängig davon, welche Methode verwendet wird, veröffentlicht und kündigt der Geräte Host das Gerät an, sobald es registriert ist. Der Unterschied zwischen den beiden Ansätzen ist, wenn der Geräte Code geladen wird. Wenn die Anwendung einen Zeiger auf das Geräte Steuerungsobjekt übergibt, wird der Geräte Code zum Zeitpunkt der Registrierung geladen und ausgeführt. Wenn die Anwendung eine ProgID übergibt, wird der Geräte Code nur geladen, wenn eine Aktion aufgerufen, eine Eigenschaft abgefragt oder eine Ereignis Abonnement Anforderung eingeht. Der zweite Ansatz ist etwas effizienter. Sie eignet sich jedoch nicht für Geräte, die vor dem Eintreffen von Steuerungs-oder Ereignis Abonnement Anforderungen ausgeführt werden müssen. bei dieser Vorgehensweise werden Geräte Steuerungs Objekte nur dann erstellt, wenn Sie benötigt werden. Diese zweite Methode kann auch zu Leistungsproblemen führen, wenn Sie die erste Anforderung für einen Gerätetyp empfängt.

Wenn Sie sicherstellen möchten, dass ein Gerät vom Geräte Host automatisch im Netzwerk angekündigt wird, wenn der Computer gestartet wird, rufen Sie [**iupnpregistranar:: registerdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)auf. **Registerdevice** stellt sicher, dass der Geräte Code nur geladen wird, wenn eine Anforderung für ein Steuerelement oder ein Ereignis Abonnement empfangen wird.

Wenn Ihre Geräte flüchtig oder überbrückt sind, rufen Sie [**iupnpregistranar:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)auf, und das Gerät wird nicht automatisch erneut angekündigt, wenn der Computer neu gestartet wird.

## <a name="discovery-announcement-lifetime"></a>Lebensdauer der Ermittlungs Ankündigung

Jedes Gerät, das beim Geräte Host registriert ist, wird einer Lebensdauer zugeordnet, die vom Gerät bei der Registrierung angegeben wird. Die Lebensdauer des Geräts ist die Zeitspanne, für die die Ermittlungs Ankündigungen des Geräts gültig sind. Die Lebensdauer wird als Header in der ersten Ermittlungs Ankündigung an den Kontrollpunkt übermittelt. Der Geräte Host aktualisiert die Ankündigung automatisch vor der Ablaufzeit. Die Werte für die Lebensdauer der Ermittlungs Ankündigung sollten 15 Minuten oder länger betragen (der Standardwert ist 30 Minuten).

## <a name="device-identifiers-created-at-registration"></a>Bei der Registrierung erstellte Geräte Bezeichner

Wenn Sie eine Geräte Beschreibungs Vorlage erstellen, muss der Geräte Entwickler den Ressourcen Pfad für die Dienst Beschreibung und zugehörige Symbole angeben. Der Ressourcen Pfad wird von der Geräte Anwendung bestimmt.

Da das gleiche Gerät mehrmals auf demselben Computer registriert werden kann, reicht der in der Vorlage für die Geräte Beschreibung angegebene udn nicht aus, um ein Gerät eindeutig zu identifizieren. Wenn ein Gerät registriert ist, erstellt der Geräte Host daher einen Geräte Bezeichner. Dieser Geräte Bezeichner kann in Verbindung mit dem udn in der Vorlage Geräte Beschreibung verwendet werden, um ein Gerät eindeutig zu identifizieren.

Dieser Bezeichner wird auch verwendet, wenn die Registrierung des Geräts vorübergehend aufgehoben und anschließend erneut registriert wird. Wenn die Registrierung eines Geräts vorübergehend aufgehoben wird, wird der udn vom Geräte Host nicht gelöscht. Folgende Gründe sind nicht zum Löschen des udn zu finden:

-   Das Gerät wird aktualisiert.
-   Sie ändern die Eigenschaften des Geräts.
-   Ein Dienst ist vorübergehend nicht verfügbar.
-   Sie fügen einem Gerät einen neuen Dienst hinzu.
-   Sie aktualisieren die dll.
-   Das Gerät befindet sich im Standbymodus.

Weitere Informationen zur Registrierung finden Sie in den folgenden Abschnitten:

-   [Registrieren eines Geräts beim Geräte Host](how-to-register-a-device-with-the-device-host.md)
-   [Aufheben der Registrierung eines Geräts](unregistering-a-device.md)
-   [**Iupnpregistranar:: unregisterdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**Iupnpreregistrinar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




