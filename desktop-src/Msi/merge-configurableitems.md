---
description: Die schreibgeschützte configurableitems-Eigenschaft des Merge-Objekts gibt eine Sammlung configurableitem-Objekte zurück, die jeweils eine einzelne Zeile aus der ModuleConfiguration-Tabelle darstellen.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configurableitems-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359339"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="dd793-103">Merge.Configurableitems (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dd793-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="dd793-104">Die schreibgeschützte **configurableitems** -Eigenschaft des [**Merge**](merge-object.md) -Objekts gibt eine Sammlung [**configurableitem**](configurableitem-object.md) -Objekte zurück, die jeweils eine einzelne Zeile aus der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)darstellen.</span><span class="sxs-lookup"><span data-stu-id="dd793-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="dd793-105">Semantisch stellt jede Schnittstelle im Enumerator ein Element dar, das vom modulconsumer konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd793-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="dd793-106">Die-Auflistung ist eine schreibgeschützte Auflistung und implementiert die standardmäßigen schreibgeschützten-Auflistungs Schnittstellen von Item (), count () und \_ netwenum ().</span><span class="sxs-lookup"><span data-stu-id="dd793-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="dd793-107">Der **ienummsmconfigitems** -Enumerator implementiert Next (), Skip (), Reset () und Clone () mit der Standard Semantik.</span><span class="sxs-lookup"><span data-stu-id="dd793-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="dd793-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dd793-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd793-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd793-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="dd793-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dd793-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="dd793-111">C++</span><span class="sxs-lookup"><span data-stu-id="dd793-111">C++</span></span>

<span data-ttu-id="dd793-112">Weitere Informationen finden [**Sie unter Get \_ configurableitems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span><span class="sxs-lookup"><span data-stu-id="dd793-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd793-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd793-113">Requirements</span></span>



| <span data-ttu-id="dd793-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd793-114">Requirement</span></span> | <span data-ttu-id="dd793-115">Wert</span><span class="sxs-lookup"><span data-stu-id="dd793-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd793-116">Version</span><span class="sxs-lookup"><span data-stu-id="dd793-116">Version</span></span><br/> | <span data-ttu-id="dd793-117">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dd793-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="dd793-118">Header</span><span class="sxs-lookup"><span data-stu-id="dd793-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dd793-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd793-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd793-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dd793-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd793-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd793-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




