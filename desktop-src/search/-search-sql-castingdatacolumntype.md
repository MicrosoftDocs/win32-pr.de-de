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
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="3c7fc-103">Umwandeln des Datentyps einer Spalte</span><span class="sxs-lookup"><span data-stu-id="3c7fc-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="3c7fc-104">Manchmal müssen Sie Zeichen folgen Daten, die aus Dokumenten extrahiert werden, als einen anderen Datentyp umwandeln, damit ein entsprechender Vergleich erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="3c7fc-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="3c7fc-105">Wandeln Sie mithilfe der folgenden Syntax einen Bezeichner oder einen literalen in einen anderen Datentyp um:</span><span class="sxs-lookup"><span data-stu-id="3c7fc-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="3c7fc-106">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3c7fc-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="3c7fc-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c7fc-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c7fc-108">Datentypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="3c7fc-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



