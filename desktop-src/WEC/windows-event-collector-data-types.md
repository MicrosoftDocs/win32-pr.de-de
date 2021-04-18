---
title: Windows-Ereignis Sammler Datentypen (evcoll. h)
description: Die Datentypen für die Windows-Ereignis Sammlung werden als Objektvariablen Typen für Ereignis Abonnements, Funktionsparameter Typen und Funktions Rückgabe Typen verwendet.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340556"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="29bfd-105">Windows-Ereignis Sammler Datentypen</span><span class="sxs-lookup"><span data-stu-id="29bfd-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="29bfd-106">Die Datentypen für die Windows-Ereignis Sammlung werden als Objektvariablen Typen für Ereignis Abonnements, Funktionsparameter Typen und Funktions Rückgabe Typen verwendet.</span><span class="sxs-lookup"><span data-stu-id="29bfd-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="29bfd-107">**EC- \_ handle**</span><span class="sxs-lookup"><span data-stu-id="29bfd-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="29bfd-108">Handle für ein Abonnement Objekt.</span><span class="sxs-lookup"><span data-stu-id="29bfd-108">Handle to a subscription object.</span></span> <span data-ttu-id="29bfd-109">Wird zur Darstellung eines Ereignis Sammler Abonnements verwendet.</span><span class="sxs-lookup"><span data-stu-id="29bfd-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="29bfd-110">**Eigenschaften Handle für EC- \_ Objekt \_ array \_ \_**</span><span class="sxs-lookup"><span data-stu-id="29bfd-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="29bfd-111">Handle für ein Array von Eigenschafts Werten für die Ereignis Quellen eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="29bfd-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="29bfd-112">Das Array Handle wird von der [**ecgetabonneptionproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) -Methode zurückgegeben, wenn der **ecabonptioneventsources** -Wert an den *PropertyId* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="29bfd-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29bfd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29bfd-113">Requirements</span></span>



| <span data-ttu-id="29bfd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29bfd-114">Requirement</span></span> | <span data-ttu-id="29bfd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="29bfd-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29bfd-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29bfd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="29bfd-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29bfd-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="29bfd-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29bfd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="29bfd-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29bfd-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="29bfd-120">Header</span><span class="sxs-lookup"><span data-stu-id="29bfd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="29bfd-121"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="29bfd-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





