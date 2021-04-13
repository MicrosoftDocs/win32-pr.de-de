---
title: Erstellen und Ausführen einer Ansicht
description: Sie können eine Ansicht für Daten erstellen, die aus Active Directory abgerufen werden. Beachten Sie, dass nur die Sicht Definition in SQL Server und nicht im eigentlichen Resultset gespeichert wird. Daher erhalten Sie möglicherweise ein anderes Ergebnis, wenn Sie die Ansicht zu einem späteren Zeitpunkt aufrufen.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387964"
---
# <a name="creating-and-executing-a-view"></a>Erstellen und Ausführen einer Ansicht

Sie können eine Ansicht für Daten erstellen, die aus Active Directory abgerufen werden. Beachten Sie, dass nur die Sicht Definition in SQL Server und nicht im eigentlichen Resultset gespeichert wird. Daher erhalten Sie möglicherweise ein anderes Ergebnis, wenn Sie die Ansicht zu einem späteren Zeitpunkt aufrufen.

Im folgenden Codebeispiel wird gezeigt, wie eine Sicht erstellt wird.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Verwenden Sie den folgenden Code, um eine Ansicht aufzurufen.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines heterogenen Joins zwischen SQL Server und Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




