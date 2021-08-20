---
description: Nach der SELECT-Anweisung verwenden Sie die FROM-Klausel, um anzugeben, wo nach übereinstimmenden Dokumenten gesucht werden soll.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6231244df2a2ec8753950ccb1a7d046c3510eff6582215d0aa3d71ebc127e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863396"
---
# <a name="from-clause"></a>FROM-Klausel

Nach der SELECT-Anweisung verwenden Sie die FROM-Klausel, um anzugeben, wo nach übereinstimmenden Dokumenten gesucht werden soll. Im Folgenden finden Sie die Syntax der FROM-Klausel für eine lokale Abfrage:


```
FROM [<ComputerName>.]SystemIndex
```



Derzeit unterstützt Windows Search nur einen Katalog, SystemIndex. Um den lokalen Katalog eines Remotecomputers abzufragen, fügen Sie den Computernamen vor dem Katalog und einen UNC-Pfad (Universal Naming Convention) auf dem Remotecomputer in die SCOPE- oder DIRECTORY-Klausel ein.

Sie geben einen Bereich als Einschränkung in der WHERE-Klausel an, wie im Thema [SCOPE- und DIRECTORY-Prädikate](-search-sql-folderdepth.md) beschrieben.

## <a name="examples"></a>Beispiele


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



Im zweiten der vorherigen Beispiele ist die Abfrage auf einen Remotecomputer mit dem Namen "zarascomputer" ausgerichtet. Beachten Sie, dass dieser Computername sowohl in der FROM- als auch in der SCOPE-Klausel angezeigt wird. Im dritten Beispiel ist die Abfrage auf einen Freigabenamen "users" auf einem Server mit dem Namen "server" ausgerichtet (wobei der UNC-Pfad \\ \\ \\ Serverbenutzer wäre).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Übersicht über die Syntax für SQL Suchen](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[SELECT-Anweisung](-search-sql-select.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

[SCOPE- und DIRECTORY-Prädikate](-search-sql-folderdepth.md)
</dt> </dl>

 

 



