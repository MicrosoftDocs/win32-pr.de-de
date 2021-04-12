---
description: Der viewspaces-Qualifizierer definiert die Namen und den Speicherort der Namespaces, in denen sich die Quell Instanzen befinden. Sie können eine beliebige Kombination von Namespaces auf lokalen Computern oder Remote Computern angeben.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Viewspaces Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218290"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="bffc5-104">Viewspaces Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="bffc5-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="bffc5-105">Der **viewspaces-Qualifizierer** definiert die Namen und den Speicherort der Namespaces, in denen sich die Quell Instanzen befinden.</span><span class="sxs-lookup"><span data-stu-id="bffc5-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="bffc5-106">Sie können eine beliebige Kombination von Namespaces auf lokalen Computern oder Remote Computern angeben.</span><span class="sxs-lookup"><span data-stu-id="bffc5-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="bffc5-107">Im folgenden Beispiel werden zwei Namespaces auf dem lokalen Computer aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bffc5-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="bffc5-108">Der [Ansichts Anbieter](view-provider.md) entspricht den Quell Abfragen im Ansichts [Quellen-Qualifizierer](viewsources-qualifier.md) mit den Namespaces, die im **viewspaces** -Qualifizierer in der Reihenfolge aufgeführt sind, in der die Abfragen und Namespaces aufgelistet</span><span class="sxs-lookup"><span data-stu-id="bffc5-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="bffc5-109">Normalerweise besteht eine eins-zu-eins-Beziehung zwischen der Anzahl der Namespaces **, die im** Ansichts Bereichs Qualifizierer aufgelistet sind, und den Abfragen, die im **viewsources** -Qualifizierer aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bffc5-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="bffc5-110">In einigen Fällen möchten Sie möglicherweise, dass die im viewsources-Qualifizierer aufgelisteten Abfragen für zwei oder mehr Namespaces ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bffc5-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="bffc5-111">Sie können einen doppelten Doppelpunkt "::" verwenden, um mehrere Namespaces zu trennen, die von einer der Abfragen im **viewsources** -Array ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="bffc5-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="bffc5-112">Im folgenden Beispiel wird die erste Abfrage im [**viewsources**](viewsources-qualifier.md) -Array für den Namespace im ersten paar von Anführungszeichen, die zweite Abfrage für die drei Namespaces im zweiten paar von Anführungszeichen und die dritte Abfrage für die beiden Namespaces im dritten paar von Anführungszeichen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bffc5-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="bffc5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bffc5-113">Requirements</span></span>



| <span data-ttu-id="bffc5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bffc5-114">Requirement</span></span> | <span data-ttu-id="bffc5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bffc5-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bffc5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bffc5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bffc5-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bffc5-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bffc5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bffc5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bffc5-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bffc5-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bffc5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bffc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffc5-121">**Spezifische Qualifizierer für den Ansichts Anbieter**</span><span class="sxs-lookup"><span data-stu-id="bffc5-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




