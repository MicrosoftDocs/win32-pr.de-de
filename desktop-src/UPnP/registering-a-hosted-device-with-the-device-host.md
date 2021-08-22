---
title: Registrieren eines gehosteten Geräts beim Gerätehost
description: Das Registrieren eines gehosteten Geräts bedeutet, dem Gerätehost die Gerätebeschreibung und das Gerätesteuerungsobjekt zur Verfügung zu stellen.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486d01364b684e2aa6792b8a6c0b91ccc87a26670057c67192fe587ac049c388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999560"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registrieren eines gehosteten Geräts beim Gerätehost

Das Registrieren eines gehosteten Geräts bedeutet, dem Gerätehost die Gerätebeschreibung und das Gerätesteuerungsobjekt zur Verfügung zu stellen. Der Gerätehost erstellt dann eine vollständige UPnP-Gerätebeschreibung, veröffentlicht sie und kündigt das Gerät im Netzwerk mithilfe des UPnP-Ermittlungsprotokolls an. Sobald ein Gerät veröffentlicht wurde, ist es für Steuerungspunkte verfügbar.

Geräte werden auf zwei Arten registriert:

-   Eine Anwendung erstellt eine Instanz des Gerätesteuerungsobjekts und übergibt einen Zeiger darauf an den Gerätehost.
-   Die Anwendung übergibt die ProgID für ein registriertes Gerätesteuerungsobjekt an den Gerätehost. Der Gerätehost instanziiert sie, wenn der Gerätehost die erste Anforderung für das Gerät empfängt.

Unabhängig davon, welche Methode verwendet wird, veröffentlicht und kündigt der Gerätehost das Gerät an, sobald es registriert ist. Der Unterschied zwischen den beiden Ansätzen hat mit dem Laden des Gerätecodes zu tun. Wenn die Anwendung einen Zeiger auf das Gerätesteuerungsobjekt übergibt, wird der Gerätecode geladen und zum Zeitpunkt der Registrierung ausgeführt. Wenn die Anwendung eine ProgID übergibt, wird der Gerätecode nur geladen, wenn eine Aktion aufgerufen wird, eine Eigenschaft abgefragt wird oder eine Ereignisabonnementanforderung eingeht. Der zweite Ansatz ist etwas effizienter. Sie ist jedoch nicht für Geräte geeignet, die ausgeführt werden müssen, bevor Steuerungs- oder Ereignisabonnementanforderungen eintreffen, da bei diesem Ansatz Gerätesteuerungsobjekte nur erstellt werden, wenn sie benötigt werden. Diese zweite Methode kann auch Leistungsprobleme erzeugen, wenn sie die erste Anforderung für einen Gerätetyp empfängt.

Wenn Sie sicherstellen möchten, dass ein Gerät automatisch vom Gerätehost im Netzwerk angekündigt wird, wenn der Computer gestartet wird, rufen Sie [**IUPnPRegistrar::RegisterDevice auf.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) **RegisterDevice stellt** sicher, dass Ihr Gerätecode nur geladen wird, wenn eine Steuerelement- oder Ereignisabonnementanforderung empfangen wird.

Wenn Ihre Geräte vorübergehend oder überbrückt sind, rufen Sie [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)auf, und das Gerät wird nicht automatisch erneut angekündigt, wenn der Computer neu gestartet wird.

## <a name="discovery-announcement-lifetime"></a>Lebensdauer der Ermittlungsankündigung

Jedes gerät, das beim Gerätehost registriert ist, ist einer Lebensdauer zugeordnet, die vom Gerät bei der Registrierung angegeben wird. Die Lebensdauer des Geräts ist der Zeitraum, für den die Ermittlungsankündigungen des Geräts gültig sind. Die Lebensdauer wird an den Kontrollpunkt als Header in der ersten Ermittlungsankündigung übergeben. Der Gerätehost aktualisiert die Ankündigung automatisch vor der Ablaufzeit. Die Werte für die Lebensdauer der Ermittlungsankündigung sollten 15 Minuten oder mehr sein (der Standardwert ist 30 Minuten).

## <a name="device-identifiers-created-at-registration"></a>Bei der Registrierung erstellte Gerätebezeichner

Beim Erstellen einer Gerätebeschreibungsvorlage muss der Geräteentwickler den Ressourcenpfad zur Dienstbeschreibung und den zugehörigen Symbolen bereitstellen. Der Ressourcenpfad wird von der Geräteanwendung bestimmt.

Da dasselbe Gerät mehrmals auf demselben Computer registriert werden kann, reicht die in der Gerätebeschreibungsvorlage angegebene UDN nicht aus, um ein Gerät eindeutig zu identifizieren. Daher erstellt der Gerätehost bei der Registrierung eines Geräts eine Geräte-ID. Dieser Gerätebezeichner kann in Verbindung mit dem UDN in der Gerätebeschreibungsvorlage verwendet werden, um ein Gerät eindeutig zu identifizieren.

Dieser Bezeichner wird auch verwendet, wenn die Registrierung des Geräts vorübergehend aufgehoben und dann erneut registriert wird. Wenn die Registrierung eines Geräts vorübergehend aufgehoben wird, löscht der Gerätehost den UDN nicht. Gründe für das Nichtlöschen der UDN sind:

-   Das Gerät wird aktualisiert.
-   Sie ändern die Eigenschaften des Geräts.
-   Ein Dienst ist vorübergehend nicht verfügbar.
-   Sie fügen einem Gerät einen neuen Dienst hinzu.
-   Sie aktualisieren die DLL.
-   Das Gerät befindet sich im Stand-by-Modus.

Weitere Informationen zur Registrierung finden Sie in den folgenden Abschnitten:

-   [Registrieren eines Geräts beim Gerätehost](how-to-register-a-device-with-the-device-host.md)
-   [Aufheben der Registrierung eines Geräts](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




