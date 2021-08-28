---
title: Serverlose Bindung und RootDSE
description: Coden Sie einen Servernamen nach Möglichkeit nicht hart.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Serverlose Bindung und RootDSE AD
- Serverloses Bindungs-AD
- RootDSE AD
- Active Directory, Using, Binding, Serverless Binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a2b567ebfae52a316dce59c3bc6ab442780e61
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881231"
---
# <a name="serverless-binding-and-rootdse"></a>Serverlose Bindung und RootDSE

Coden Sie einen Servernamen nach Möglichkeit nicht hart. Darüber hinaus sollte die Bindung in den meisten Fällen nicht unnötigerweise an einen einzelnen Server gebunden werden. Active Directory Domain Services serverlose Bindung unterstützen, was bedeutet, dass Active Directory in der Standarddomäne gebunden werden kann, ohne den Namen eines Domänencontrollers anzugeben. Bei normalen Anwendungen ist dies in der Regel die Domäne des angemeldeten Benutzers. Bei Dienstanwendungen ist dies entweder die Domäne des Dienstanmeldungskontos oder die Domäne des Clients, für den der Dienst die Identität angenommen hat.

In LDAP 3.0 ist rootDSE als Stamm der Verzeichnisdatenstruktur auf einem Verzeichnisserver definiert. RootDSE ist nicht Teil eines Namespace. Der Zweck von rootDSE besteht in der Bereitstellung von Daten über den Verzeichnisserver. Im Folgenden finden Sie die Bindungszeichenfolge, die zum Binden an rootDSE verwendet wird.


```C++
LDAP://<servername>/rootDSE
```



Der &lt; Servername &gt; ist der DNS-Name eines Servers. Der &lt; Servername &gt; ist optional, wie im folgenden Format gezeigt.


```C++
LDAP://rootDSE
```



In diesem Fall wird ein Standarddomänencontroller aus der Domäne verwendet, in der sich der Sicherheitskontext des aufrufenden Threads befindet. Wenn innerhalb des Standorts nicht auf einen Domänencontroller zugegriffen werden kann, wird der erste Domänencontroller verwendet, der gefunden werden kann.

RootDSE ist ein bekannter und zuverlässiger Speicherort auf jedem Verzeichnisserver, um Distinguished Names der Domäne, des Schemas und der Konfigurationscontainer sowie andere Daten über den Server und den Inhalt seiner Verzeichnisdatenstruktur zu erhalten. Diese Eigenschaften ändern sich selten auf einem bestimmten Server. Eine Anwendung kann diese Eigenschaften beim Start lesen und während der gesamten Sitzung verwenden.

Zusammenfassend sollte eine Anwendung eine serverlose Bindung verwenden, um eine Bindung an das Verzeichnis in der aktuellen Domäne herzustellen, rootDSE verwenden, um den Distinguished Name für einen Namespace zu erhalten, und diesen Distinguished Name zum Binden an Objekte im Namespace verwenden.

Weitere Informationen zu Attributen, die von rootDSE unterstützt werden, finden Sie unter [RootDSE](/windows/desktop/ADSchema/rootdse) in der Dokumentation zum Active Directory-Schema.

Weitere Informationen und ein Codebeispiel, das zeigt, wie serverlose Bindung und rootDSE verwendet werden, finden Sie unter [Beispielcode zum](example-code-for-getting-the-distinguished-name-of-the-domain.md)Abrufen des Distinguished Name der Domäne .

 

 
