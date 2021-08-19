---
title: Erstellen und Ausführen einer Ansicht
description: Sie können eine Ansicht für Daten erstellen, die aus Active Directory abgerufen werden. Beachten Sie, dass nur die Ansichtsdefinition in SQL Server und nicht im tatsächlichen Resultset gespeichert wird. Daher erhalten Sie möglicherweise ein anderes Ergebnis, wenn Sie die Ansicht zu einem späteren Zeitpunkt aufrufen.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c4676154ea32dd06e39498e9f943b55d8dbf39694ab9c1005e942cad85f7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082724"
---
# <a name="creating-and-executing-a-view"></a>Erstellen und Ausführen einer Ansicht

Sie können eine Ansicht für Daten erstellen, die aus Active Directory abgerufen werden. Beachten Sie, dass nur die Ansichtsdefinition in SQL Server und nicht im tatsächlichen Resultset gespeichert wird. Daher erhalten Sie möglicherweise ein anderes Ergebnis, wenn Sie die Ansicht zu einem späteren Zeitpunkt aufrufen.

Im folgenden Codebeispiel wird das Erstellen einer Ansicht veranschaulicht.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Verwenden Sie den folgenden Code, um eine Sicht aufzurufen.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines heterogenen Joins zwischen SQL Server und Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




