---
description: Alle Ansichts Klassen müssen über einen Zeichen folgen Array-Qualifizierer namens viewsources verfügen.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Viewsources Qualifizierer
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
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757759"
---
# <a name="viewsources-qualifier"></a>Viewsources Qualifizierer

Alle Ansichts Klassen müssen über einen Zeichen folgen Array-Qualifizierer namens **viewsources** verfügen. Der **viewsources** -Qualifizierer enthält die Quell Abfragen, die die in der Ansichts Klasse verwendeten Quell Instanzen definieren. Der Wert des **viewsources** -Qualifizierers ist ein Zeichen folgen Array, das WMI Query Language-Abfragen [*(WQL)*](gloss-w.md) enthält. Sie können Quell Klassen definieren und die Quell Instanzen einschränken, die ihre Ansichts Klasse mit der [Abfrage with WQL](querying-with-wql.md)[WHERE-Klausel](where-clause.md) verwendet, um eine gefilterte Ansicht zu erstellen.

Der [Ansichts Anbieter](view-provider.md) entspricht den Quell Abfragen im Ansichts **Quellen** -Qualifizierer mit den Namespaces, die im [viewspaces-Qualifizierer](viewspaces-qualifier.md) in der Reihenfolge aufgeführt sind, in der die Abfragen und Namespaces aufgelistet Die Anzahl der Quell Abfragen muss mit der Anzahl der Namespaces identisch sein, die im viewspaces-Qualifizierer aufgelistet sind. Die Reihenfolge, in der Sie die Quell Abfragen auflisten, bestimmt die Namespaces, von denen die Quell Instanzen gezeichnet werden.

Im folgenden Beispiel werden nur Instanzen der **localdisk** -Klasse ausgewählt, wobei der Wert der **File System** -Eigenschaft "NTFS" ist, und Instanzen der Klasse " **remotedisk** ", bei denen der Wert der **FreeSpace** -Eigenschaft größer als 45 Megabyte ist:


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
> Die Anzahl der Quell Abfragen, die Sie für Verknüpfungs Ansichts Klassen definieren können, hängt von der Anzahl der Instanzen ab, die von diesen Abfragen zurückgegeben werden, und der Anzahl der Möglichkeiten, mit denen Die Anzahl möglicher Kombinationen von Quell Instanzen für Ansichts Klassen wächst exponentiell, sodass Sie Quell Abfragen für joinansichts Klassen so einfach wie möglich halten.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Spezifische Qualifizierer für den Ansichts Anbieter**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




