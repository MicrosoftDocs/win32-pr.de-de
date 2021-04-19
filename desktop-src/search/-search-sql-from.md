---
description: Nach der SELECT-Anweisung verwenden Sie die from-Klausel, um anzugeben, wo nach übereinstimmenden Dokumenten gesucht werden soll.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346281"
---
# <a name="from-clause"></a>FROM-Klausel

Nach der SELECT-Anweisung verwenden Sie die from-Klausel, um anzugeben, wo nach übereinstimmenden Dokumenten gesucht werden soll. Im folgenden finden Sie die Syntax der from-Klausel für eine lokale Abfrage:


```
FROM [<ComputerName>.]SystemIndex
```



Derzeit unterstützt Windows Search nur einen Katalog, SystemIndex. Um den lokalen Katalog eines Remote Computers abzufragen, müssen Sie den Computernamen vor dem Katalog und einen Universal Naming Convention (UNC)-Pfad auf dem Remote Computer in der Scope-oder Directory-Klausel einschließen.

Sie geben einen Gültigkeitsbereich als Einschränkung in der WHERE-Klausel an, wie im Thema [Geltungsbereich und Verzeichnis Prädikate](-search-sql-folderdepth.md) beschrieben.

## <a name="examples"></a>Beispiele


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



Im zweiten der vorangegangenen Beispiele ist die Abfrage auf einen Remote Computer mit dem Namen "zarascomputer" ausgerichtet. Beachten Sie, dass dieser Computername in der from-Klausel und der Scope-Klausel angezeigt wird. Im dritten Beispiel zielt die Abfrage auf einen Freigabe Namen "Users" auf einem Server mit dem Namen "Server" (wobei der UNC-Pfad \\ \\ Server \\ Benutzer lauten würde).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Übersicht über die SQL-Such Syntax](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[SELECT-Anweisung](-search-sql-select.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

[Bereichs-und Verzeichnis Prädikate](-search-sql-folderdepth.md)
</dt> </dl>

 

 



