---
title: Warnung zu Aria-Datentabelle
description: Warnung zu Aria-Datentabelle
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- Ariadatatablewarningid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037484"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="b247d-104">Warnung zu Aria-Datentabelle</span><span class="sxs-lookup"><span data-stu-id="b247d-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="b247d-105">Text</span><span class="sxs-lookup"><span data-stu-id="b247d-105">Text</span></span>

<span data-ttu-id="b247d-106">Die Tabelle enthält Daten, hat aber weder eine Zusammenfassung noch ein gültiges **Aria-DescribedBy** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="b247d-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="b247d-107">type</span><span class="sxs-lookup"><span data-stu-id="b247d-107">Type</span></span>

<span data-ttu-id="b247d-108">Warnung</span><span class="sxs-lookup"><span data-stu-id="b247d-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="b247d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b247d-109">Description</span></span>

<span data-ttu-id="b247d-110">Diese Warnung gilt für HTML-Tabellen mit mehr als einer Zelle.</span><span class="sxs-lookup"><span data-stu-id="b247d-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="b247d-111">Sie gilt nicht für Tabellen mit, `role="presentation"` da diese als Layouttabellen angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="b247d-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="b247d-112">Diese Warnung gibt an, dass die Tabelle als Datentabelle identifiziert ist, aber keine barrierefreie Beschreibung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b247d-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="b247d-113">Nicht für alle Datentabellen ist eine barrierefreie Beschreibung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b247d-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="b247d-114">Sie sollten eine barrierefreie Beschreibung definieren, wenn Benutzer weitere Informationen benötigen, um die Struktur und den Inhalt der Datentabelle zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="b247d-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="b247d-115">Um diese Warnung zu beheben, definieren Sie eine Tabelle, auf die zugegriffen werden kann, indem Sie das Summary-Attribut oder das **Aria-DescribedBy** -Attribut verwenden</span><span class="sxs-lookup"><span data-stu-id="b247d-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="b247d-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b247d-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




