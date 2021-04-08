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
# <a name="viewsources-qualifier"></a><span data-ttu-id="16081-103">Viewsources Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="16081-103">ViewSources Qualifier</span></span>

<span data-ttu-id="16081-104">Alle Ansichts Klassen müssen über einen Zeichen folgen Array-Qualifizierer namens **viewsources** verfügen.</span><span class="sxs-lookup"><span data-stu-id="16081-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="16081-105">Der **viewsources** -Qualifizierer enthält die Quell Abfragen, die die in der Ansichts Klasse verwendeten Quell Instanzen definieren.</span><span class="sxs-lookup"><span data-stu-id="16081-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="16081-106">Der Wert des **viewsources** -Qualifizierers ist ein Zeichen folgen Array, das WMI Query Language-Abfragen [*(WQL)*](gloss-w.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="16081-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="16081-107">Sie können Quell Klassen definieren und die Quell Instanzen einschränken, die ihre Ansichts Klasse mit der [Abfrage with WQL](querying-with-wql.md)[WHERE-Klausel](where-clause.md) verwendet, um eine gefilterte Ansicht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="16081-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="16081-108">Der [Ansichts Anbieter](view-provider.md) entspricht den Quell Abfragen im Ansichts **Quellen** -Qualifizierer mit den Namespaces, die im [viewspaces-Qualifizierer](viewspaces-qualifier.md) in der Reihenfolge aufgeführt sind, in der die Abfragen und Namespaces aufgelistet</span><span class="sxs-lookup"><span data-stu-id="16081-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="16081-109">Die Anzahl der Quell Abfragen muss mit der Anzahl der Namespaces identisch sein, die im viewspaces-Qualifizierer aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="16081-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="16081-110">Die Reihenfolge, in der Sie die Quell Abfragen auflisten, bestimmt die Namespaces, von denen die Quell Instanzen gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="16081-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="16081-111">Im folgenden Beispiel werden nur Instanzen der **localdisk** -Klasse ausgewählt, wobei der Wert der **File System** -Eigenschaft "NTFS" ist, und Instanzen der Klasse " **remotedisk** ", bei denen der Wert der **FreeSpace** -Eigenschaft größer als 45 Megabyte ist:</span><span class="sxs-lookup"><span data-stu-id="16081-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


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
> <span data-ttu-id="16081-112">Die Anzahl der Quell Abfragen, die Sie für Verknüpfungs Ansichts Klassen definieren können, hängt von der Anzahl der Instanzen ab, die von diesen Abfragen zurückgegeben werden, und der Anzahl der Möglichkeiten, mit denen</span><span class="sxs-lookup"><span data-stu-id="16081-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="16081-113">Die Anzahl möglicher Kombinationen von Quell Instanzen für Ansichts Klassen wächst exponentiell, sodass Sie Quell Abfragen für joinansichts Klassen so einfach wie möglich halten.</span><span class="sxs-lookup"><span data-stu-id="16081-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16081-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16081-114">Requirements</span></span>



| <span data-ttu-id="16081-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16081-115">Requirement</span></span> | <span data-ttu-id="16081-116">Wert</span><span class="sxs-lookup"><span data-stu-id="16081-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="16081-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16081-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16081-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16081-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="16081-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16081-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16081-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16081-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16081-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16081-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16081-122">**Spezifische Qualifizierer für den Ansichts Anbieter**</span><span class="sxs-lookup"><span data-stu-id="16081-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




