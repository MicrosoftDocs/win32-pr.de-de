---
title: Serverlose Bindung und RootDSE
description: Programmieren Sie einen Servernamen nach Möglichkeit nicht hart.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Serverlose Bindung und RootDSE AD
- Serverloses Bindungs-AD
- RootDSE AD
- Active Directory, Using, Binding, Serverless Binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c88386ae95efdebd031199e135ff4c5d610e402b9cba522256df5eef097e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024928"
---
# <a name="serverless-binding-and-rootdse"></a>Serverlose Bindung und RootDSE

Programmieren Sie einen Servernamen nach Möglichkeit nicht hart. Darüber hinaus sollte die Bindung in den meisten Fällen nicht unnötigerweise an einen einzelnen Server gebunden werden. Active Directory Domain Services unterstützen die serverlose Bindung. Dies bedeutet, dass Active Directory in der Standarddomäne gebunden werden kann, ohne den Namen eines Domänencontrollers anzugeben. Bei normalen Anwendungen ist dies in der Regel die Domäne des angemeldeten Benutzers. Bei Dienstanwendungen ist dies entweder die Domäne des Dienstanmeldungskontos oder die Domäne des Clients, für den der Dienst die Identität angenommen hat.

In LDAP 3.0 wird rootDSE als Stamm der Verzeichnisdatenstruktur auf einem Verzeichnisserver definiert. RootDSE ist nicht Teil eines Namespaces. Der Zweck des rootDSE besteht darin, Daten über den Verzeichnisserver bereitzustellen. Es folgt die Bindungszeichenfolge, die zum Binden an rootDSE verwendet wird.


```C++
LDAP://<servername>/rootDSE
```



<servername>ist der DNS-Name eines Servers. ist <servername> optional, wie im folgenden Format gezeigt.


```C++
LDAP://rootDSE
```



In diesem Fall wird ein Standarddomänencontroller aus der Domäne verwendet, in der sich der Sicherheitskontext des aufrufenden Threads befindet. Wenn innerhalb des Standorts nicht auf einen Domänencontroller zugegriffen werden kann, wird der erste gefundene Domänencontroller verwendet.

RootDSE ist ein bekannter und zuverlässiger Speicherort auf jedem Verzeichnisserver, um Distinguished Names der Domänen-, Schema- und Konfigurationscontainer sowie andere Daten über den Server und den Inhalt der Verzeichnisdatenstruktur abzurufen. Diese Eigenschaften ändern sich auf einem bestimmten Server nur selten. Eine Anwendung kann diese Eigenschaften beim Start lesen und während der gesamten Sitzung verwenden.

Zusammengefasst: Eine Anwendung sollte eine serverlose Bindung verwenden, um eine Bindung an das Verzeichnis in der aktuellen Domäne zu erstellen, rootDSE verwenden, um den Distinguished Name für einen Namespace abzurufen, und diesen Distinguished Name zum Binden an Objekte im Namespace verwenden.

Weitere Informationen zu attributen, die von rootDSE unterstützt werden, finden Sie unter [RootDSE](/windows/desktop/ADSchema/rootdse) in der Dokumentation zum Active Directory-Schema.

Weitere Informationen und ein Codebeispiel, das die Verwendung von serverloser Bindung und rootDSE veranschaulicht, finden Sie unter [Beispielcode zum Abrufen des Distinguished Name der Domäne.](example-code-for-getting-the-distinguished-name-of-the-domain.md)

 

 