---
title: Aufheben der Registrierung eines Geräts
description: Verwenden Sie die iupnpregistrinsterdevice-Methode, um die Registrierung eines Geräts aufzuheben.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c480433e3d8dbf4ff823728281018801ec35c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471668"
---
# <a name="unregistering-a-device"></a>Aufheben der Registrierung eines Geräts

Verwenden Sie die [**iupnpregistrannpregistranar:: unregisterdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) -Methode, um die Registrierung eines Geräts aufzuheben. Abhängig vom Wert von " *spermanent*" kann die Registrierung des Geräts (entfernt vom Geräte Host) vorübergehend oder dauerhaft aufgehoben werden. Entwickler sollten Geräte vorübergehend entfernen, wenn die Geräte neu registriert werden und die Geräte denselben udn verwenden sollten. Andernfalls werden die Geräte dauerhaft entfernt.

Der GUID, der zum Aufheben der Registrierung verwendet wird, ist nicht der udn. Sie müssen die ID verwenden, die für Sie von [**iupnpregistraut:: registerdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) oder [**iupnpregistrear:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)zurückgegeben wurde.

> [!Note]  
> Sie können das [**iupnpregistrinar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) -Objekt freigeben. Nur die ID muss zwischengespeichert werden.

 

Wenn " *f* " den Wert " **false**" hat, wird das Gerät vorübergehend entfernt. Verwenden Sie [**iupnpreregistrear**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) Interface, um das Gerät erneut zu registrieren. Die Methoden [**iupnpreregistrinar:: reregisterdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) und [**iupnpreregistrinar:: reregisterrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) verwenden im Fall von zuvor vom Geräte Host für das nicht registrierte Gerät generierten Geräten dieselbe udn oder udns.

Wenn " *spermanent* " den Wert " **true**" hat, wird das Gerät dauerhaft vom Geräte Host entfernt. Wenn Sie dieses Gerät erneut auf demselben Computer registrieren, wird ein anderes udn erstellt als zuvor erstellt.

> [!Note]  
> Wenn ein Gerät mehrmals auf demselben Computer registriert ist, generiert der Geräte Host verschiedene udns für jede Instanz des Geräts.

 

 

 




