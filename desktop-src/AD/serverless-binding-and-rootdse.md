---
title: Server lose Bindung und RootDSE
description: Wenn möglich, sollten Sie einen Servernamen nicht hart codieren.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Server lose Bindung und RootDSE-AD
- Server lose Bindungs Anzeige
- RootDSE-AD
- Active Directory, verwenden, Bindung, Server lose Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472484"
---
# <a name="serverless-binding-and-rootdse"></a>Server lose Bindung und RootDSE

Wenn möglich, sollten Sie einen Servernamen nicht hart codieren. Außerdem sollte die Bindung unter den meisten Umständen nicht unnötig an einen einzelnen Server gebunden werden. Active Directory Domain Services unterstützen die Server lose Bindung, was bedeutet, dass Active Directory an die Standard Domäne gebunden werden kann, ohne den Namen eines Domänen Controllers anzugeben. Für normale Anwendungen ist dies in der Regel die Domäne des angemeldeten Benutzers. Bei Dienst Anwendungen ist dies entweder die Domäne des Dienst Anmelde Kontos oder die des Clients, dessen Identität der Dienst annimmt.

In LDAP 3,0 ist RootDSE als Stammverzeichnis der Verzeichnis Datenstruktur auf einem Verzeichnisserver definiert. RootDSE ist nicht Teil eines Namespace. Der Zweck von RootDSE besteht darin, Daten zum Verzeichnisserver bereitzustellen. Im folgenden finden Sie die Bindungs Zeichenfolge, die verwendet wird, um eine Bindung an RootDSE herzustellen.


```C++
LDAP://<servername>/rootDSE
```



Der <servername> ist der DNS-Name eines Servers. Der <servername> ist optional, wie im folgenden Format dargestellt.


```C++
LDAP://rootDSE
```



In diesem Fall wird ein Standard Domänen Controller aus der Domäne verwendet, in der der Sicherheitskontext des aufrufenden Threads verwendet wird. Wenn innerhalb des Standorts nicht auf einen Domänen Controller zugegriffen werden kann, wird der erste Domänen Controller verwendet, der gefunden wird.

RootDSE ist ein bekannter und zuverlässiger Speicherort auf jedem Verzeichnisserver, um Distinguished Names der Domäne, des Schemas und der Konfigurations Container sowie anderer Daten zum Server und zum Inhalt der Verzeichnis Datenstruktur zu erhalten. Diese Eigenschaften ändern sich nur selten auf einem bestimmten Server. Eine Anwendung kann diese Eigenschaften beim Start Lesen und in der gesamten Sitzung verwenden.

Zusammenfassend sollte eine Anwendung eine Server lose Bindung verwenden, um Sie an das Verzeichnis in der aktuellen Domäne zu binden, mithilfe von RootDSE den Distinguished Name für einen Namespace zu erhalten und den Distinguished Name für die Bindung an Objekte im Namespace zu verwenden.

Weitere Informationen zu Attributen, die von RootDSE unterstützt werden, finden Sie in der Active Directory-Schema Dokumentation unter [rootDSE](/windows/desktop/ADSchema/rootdse) .

Weitere Informationen und ein Codebeispiel, in dem gezeigt wird, wie Sie die Server lose Bindung und RootDSE verwenden, finden Sie unter [Beispielcode zum Ermitteln des Distinguished Name der Domäne](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 