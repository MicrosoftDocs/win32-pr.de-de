---
title: Offline Installation
description: Offline Installation
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player Online Stores, Offline Installation
- Online Stores, Offline Installation
- Typ 1 Online Stores, Offline Installation
- Typ 2 Online Stores, Offline Installation
- Windows Media Player Online Stores, Offline Installationen
- Online Stores, Offline Installationen
- Typ 1 Online Stores, Offline Installationen
- Typ 2 Online Stores, Offline Installationen
- Offline Installation von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856364"
---
# <a name="installing-while-offline"></a>Offline Installation

Benutzer können Windows Media Player installieren, ohne mit dem Internet verbunden zu sein. In diesem Fall findet das Windows-Media Player Setup das ServiceInfo.xml Dokument, das durch den *serviceInfo* -Befehlszeilenparameter angegeben wird. Wenn das **Schlüssel** Attribut mit dem *defaultservice* -Befehlszeilenparameter übereinstimmt, wendet Setup Informationen aus den folgenden Elementen auf Windows Media Player an:

-   FriendlyName. Der Anzeige Name des Online-Stores wird auf der Windows Media Player-Benutzeroberfläche angezeigt.
-   Farbe Die angegebenen Farben werden auf die Taskleiste und die Schaltflächen angewendet.
-   ServiceTask1, ServiceTask2 und ServiceTask3. Die untergeordneten Elemente ButtonText und buttontip werden festgelegt. Das URL-Attribut ist nicht festgelegt. Die URL wird festgelegt, sobald der Benutzer eine Verbindung mit dem Internet herstellt und Windows Media Player die Liste der Online Stores auf normale Weise abruft.
-   Bild. Die Attribute menuurl und servicelargeurl sind festgelegt. Diese URLs müssen auf Images verweisen, die Sie auf der Festplatte des Benutzers mithilfe des file://-Protokolls installiert haben.

Wenn der Benutzer versucht, den Online Store anzuzeigen, zeigt Windows Media Player eine Meldung an, in der der Benutzer darüber informiert wird, dass eine Internet Verbindung erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Color-Element**](color-element.md)
</dt> <dt>

[**FriendlyName-Element**](friendlyname-element.md)
</dt> <dt>

[**Image-Element**](image-element.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Servicinput info-Element**](serviceinfo-element.md)
</dt> <dt>

[**ServiceTask1-Element**](servicetask1-element.md)
</dt> <dt>

[**ServiceTask2-Element**](servicetask2-element.md)
</dt> <dt>

[**ServiceTask3-Element**](servicetask3-element.md)
</dt> <dt>

[**Festlegen des ersten Online Stores**](setting-the-initial-online-store.md)
</dt> <dt>

[**Einrichten von Befehlszeilen Parametern für Online Stores**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




