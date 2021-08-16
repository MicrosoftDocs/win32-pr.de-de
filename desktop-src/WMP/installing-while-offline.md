---
title: Installieren im Offlinemodus
description: Installieren im Offlinemodus
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player,Offline-Installation
- Onlineshops,Installation im Offlinemodus
- Geben Sie 1 Onlineshops ein, und installieren Sie sie im Offlinemodus.
- Geben Sie 2 Onlineshops ein, und installieren Sie sie im Offlinemodus.
- Windows Media Player,Offline-Installationen
- Onlineshops,Offline-Installationen
- 'Typ 1: Onlineshops,Offline-Installationen'
- 'Typ 2: Onlineshops,Offline-Installationen'
- Installieren von Onlineshops im Offlinemodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3051aca9634bc2c53950baa783bcf62fc6861c616facd9dc563d70d011c2459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135503"
---
# <a name="installing-while-offline"></a>Installieren im Offlinemodus

Benutzer können Windows Media Player installieren, ohne mit dem Internet verbunden zu sein. In diesem Fall sucht Windows Media Player Setup das ServiceInfo.xml, das durch den *ServiceInfo-Befehlszeilenparameter* angegeben wird. Wenn das **Key-Attribut** dem *DefaultService-Befehlszeilenparameter* entspricht, wendet setup Informationen aus den folgenden Elementen auf Windows Media Player:

-   Friendlyname. Der Angezeigte Name des Onlineshops wird auf der benutzeroberfläche Windows Media Player angezeigt.
-   Farbe Die angegebenen Farben werden auf die Taskleiste und die Schaltflächen angewendet.
-   ServiceTask1, ServiceTask2 und ServiceTask3. Die untergeordneten Elemente ButtonText und ButtonTip werden festgelegt. Das URL-Attribut ist nicht festgelegt. Die URL wird festgelegt, sobald der Benutzer eine Verbindung mit dem Internet herstellt und Windows Media Player die Liste der Onlineshops auf normale Weise abruft.
-   Bild. Die Attribute MenuURL und ServiceLargeURL werden festgelegt. Diese URLs müssen auf Images verweisen, die Sie auf der Festplatte des Benutzers mithilfe des file:// installiert haben.

Wenn der Benutzer versucht, den Onlineshop Windows Media Player zeigt eine Meldung an, die den Benutzer darüber informiert, dass eine Internetverbindung erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Color-Element**](color-element.md)
</dt> <dt>

[**FriendlyName-Element**](friendlyname-element.md)
</dt> <dt>

[**Image-Element**](image-element.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo-Element**](serviceinfo-element.md)
</dt> <dt>

[**ServiceTask1-Element**](servicetask1-element.md)
</dt> <dt>

[**ServiceTask2-Element**](servicetask2-element.md)
</dt> <dt>

[**ServiceTask3-Element**](servicetask3-element.md)
</dt> <dt>

[**Festlegen des anfänglichen Online-Store**](setting-the-initial-online-store.md)
</dt> <dt>

[**Einrichten von Befehlszeilenparametern für Onlineshops**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




