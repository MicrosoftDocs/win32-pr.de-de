---
description: Alle Ansichtsklassen müssen über einen Zeichenfolgenarrayqualifizierer namens ViewSources verfügen.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: ViewSources-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2a0cadf3e1469fbdaf347b269813e76b780348d28482a00b4de290aaf4e0f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120760"
---
# <a name="viewsources-qualifier"></a>ViewSources-Qualifizierer

Alle Ansichtsklassen müssen über einen Zeichenfolgenarrayqualifizierer namens **ViewSources verfügen.** Der **ViewSources-Qualifizierer** enthält die Quellabfragen, die die in der Ansichtsklasse verwendeten Quellinstanzen definieren. Der Wert des **ViewSources-Qualifizierers** ist ein Zeichenfolgenarray, das [*WQL-Abfragen (WMI Query Language)*](gloss-w.md) enthält. Sie können Quellklassen definieren und die Quellinstanzen einschränken, die Ihre Ansichtsklasse mit der [WHERE-Klausel querying with WQL](querying-with-wql.md)[](where-clause.md) verwendet, um eine gefilterte Sicht zu erstellen.

Der [Ansichtsanbieter](view-provider.md) gleicht die Quellabfragen im **ViewSources-Qualifizierer** mit den Namespaces ab, die im [ViewSpaces-Qualifizierer](viewspaces-qualifier.md) in der Reihenfolge aufgeführt sind, in der die Abfragen und Namespaces aufgeführt sind. Die Anzahl der Quellabfragen muss mit der Anzahl der Namespaces übereinstimmen, die im ViewSpaces-Qualifizierer aufgeführt sind. Die Reihenfolge, in der Sie die Quellabfragen auflisten, bestimmt die Namespaces, aus denen die Quellinstanzen gezeichnet werden.

Im folgenden Beispiel werden nur Instanzen der **LocalDisk-Klasse** ausgewählt, bei denen der Wert der **FileSystem-Eigenschaft** "NTFS" ist, und Instanzen der **RemoteDisk-Klasse,** bei denen der Wert der **FreeSpace-Eigenschaft** größer als 45 Megabyte ist:


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> Die Anzahl der Quellabfragen, die Sie für Joinansichtsklassen definieren können, hängt von der Anzahl der Instanzen ab, die diese Abfragen zurückgeben, und von der Anzahl der Möglichkeiten, wie diese Instanzen verknüpft werden können. Die Anzahl der möglichen Kombinationen von Quellinstanzen für Ansichtsklassen wächst exponentiell, sodass Quellabfragen für Joinansichtsklassen so einfach wie möglich gehalten werden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Qualifizierer, die für den Ansichtsanbieter spezifisch sind**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




