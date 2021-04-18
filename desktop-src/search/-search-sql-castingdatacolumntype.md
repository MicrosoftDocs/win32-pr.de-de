---
description: 'Weitere Informationen finden Sie unter: Umwandeln des Datentyps einer Spalte'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Umwandeln des Datentyps einer Spalte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344049"
---
# <a name="casting-the-data-type-of-a-column"></a>Umwandeln des Datentyps einer Spalte

Manchmal müssen Sie Zeichen folgen Daten, die aus Dokumenten extrahiert werden, als einen anderen Datentyp umwandeln, damit ein entsprechender Vergleich erfolgen kann. Wandeln Sie mithilfe der folgenden Syntax einen Bezeichner oder einen literalen in einen anderen Datentyp um:


```
CAST (<identifier> | <literal> AS <datatype>)
```



Beispiel:


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datentypzuordnungen](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



