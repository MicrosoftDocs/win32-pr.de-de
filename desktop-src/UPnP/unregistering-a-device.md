---
title: Aufheben der Registrierung eines Geräts
description: Verwenden Sie die IUPnPRegistrar UnregisterDevice-Methode, um die Registrierung eines Geräts zu aufheben.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ff8eeb99ec0ba697c301e8cc15100bd06c0323b95f4099329c46729ceba9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999490"
---
# <a name="unregistering-a-device"></a>Aufheben der Registrierung eines Geräts

Verwenden Sie [**die IUPnPRegistrar::UnregisterDevice-Methode,**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) um die Registrierung eines Geräts zu aufheben. Je nach Wert von *fPermanent* kann die Registrierung des Geräts vorübergehend oder dauerhaft aufgehoben (vom Gerätehost entfernt) werden. Entwickler sollten Geräte vorübergehend entfernen, wenn die Geräte erneut registriert werden und die Geräte denselben UDN verwenden sollten. Andernfalls werden die Geräte dauerhaft entfernt.

Die GUID, die zum Aufheben der Registrierung verwendet wird, ist nicht der UDN. Sie müssen die VON [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) oder [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)zurückgegebene ID verwenden.

> [!Note]  
> Sie können das [**IUPnPRegistrar-Objekt**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) veröffentlichen. Nur die ID muss zwischengespeichert werden.

 

Wenn *fPermanent* **false ist,** wird das Gerät vorübergehend entfernt. Verwenden [**Sie die IUPnPReregistrar-Schnittstelle,**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) um das Gerät erneut zu registrieren. Die [**Methoden IUPnPReregistrar::ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) und [**IUPnPReregistrar::ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) verwenden im Fall von geschachtelten Geräten, die zuvor vom Gerätehost für das nicht registrierte Gerät generiert wurden, die gleichen UDNs oder UDNs.

Wenn *fPermanent* **true ist,** wird das Gerät dauerhaft vom Gerätehost entfernt. Wenn Sie dieses Gerät erneut auf demselben Computer registrieren, wird eine andere UDN als die zuvor erstellte erstellt.

> [!Note]  
> Wenn ein Gerät mehrmals auf demselben Computer registriert wird, generiert der Gerätehost für jede Instanz des Geräts unterschiedliche UDNs.

 

 

 




