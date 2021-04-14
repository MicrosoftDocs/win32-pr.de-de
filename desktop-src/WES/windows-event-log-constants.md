---
title: Windows-Ereignisprotokoll Konstanten (winevt. h)
description: 'Das Windows-Ereignisprotokoll definiert die folgenden Konstanten:'
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391889"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="46b27-103">Windows-Ereignisprotokoll Konstanten</span><span class="sxs-lookup"><span data-stu-id="46b27-103">Windows Event Log Constants</span></span>

<span data-ttu-id="46b27-104">Das Windows-Ereignisprotokoll definiert die folgenden Konstanten:</span><span class="sxs-lookup"><span data-stu-id="46b27-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="46b27-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT \_ Variant \_ - \_ typmaske**</span><span class="sxs-lookup"><span data-stu-id="46b27-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46b27-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="46b27-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="46b27-107">Eine Bitmaske, die Sie zum Maskieren des arraybits des Variant-Typs verwenden, damit Sie den Datentyp des Variant-Werts ermitteln können, der in der [**EVT- \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) -Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="46b27-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="46b27-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**Array von EVT- \_ Variant- \_ Typ \_**</span><span class="sxs-lookup"><span data-stu-id="46b27-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46b27-109">128</span><span class="sxs-lookup"><span data-stu-id="46b27-109">128</span></span>
</dt> <dt>



<span data-ttu-id="46b27-110">Der **Typmember** der [**EVT- \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) -Struktur ist dieses Bit festgelegt, wenn die Variante einen Zeiger auf ein Array von Werten enthält, nicht auf den Wert selbst.</span><span class="sxs-lookup"><span data-stu-id="46b27-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="46b27-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT- \_ Lese \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="46b27-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46b27-112">0x1</span><span class="sxs-lookup"><span data-stu-id="46b27-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="46b27-113">Lese Zugriffs Steuerungs Berechtigung, die das Lesen von Informationen aus einem Ereignisprotokoll zulässt.</span><span class="sxs-lookup"><span data-stu-id="46b27-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="46b27-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT- \_ Schreib \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="46b27-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46b27-115">0x2</span><span class="sxs-lookup"><span data-stu-id="46b27-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="46b27-116">Schreibzugriffs Steuerungs Berechtigung, mit der Informationen in ein Ereignisprotokoll geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="46b27-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="46b27-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**\_ \_ Zugriff löschen**</span><span class="sxs-lookup"><span data-stu-id="46b27-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46b27-118">0x4</span><span class="sxs-lookup"><span data-stu-id="46b27-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="46b27-119">Löschen Sie die Zugriffs Steuerungs Berechtigung, mit der alle Informationen aus einem Ereignisprotokoll gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="46b27-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="46b27-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**sämtlichen \_ \_ Zugriff**</span><span class="sxs-lookup"><span data-stu-id="46b27-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46b27-121">0x7</span><span class="sxs-lookup"><span data-stu-id="46b27-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="46b27-122">Alle (lesen, schreiben, löschen und löschen) Zugriffs Steuerungs Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="46b27-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46b27-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46b27-123">Requirements</span></span>



| <span data-ttu-id="46b27-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46b27-124">Requirement</span></span> | <span data-ttu-id="46b27-125">Wert</span><span class="sxs-lookup"><span data-stu-id="46b27-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46b27-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46b27-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46b27-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46b27-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="46b27-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46b27-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46b27-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46b27-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46b27-130">Header</span><span class="sxs-lookup"><span data-stu-id="46b27-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="46b27-131"><dt>Winevt. h</dt></span><span class="sxs-lookup"><span data-stu-id="46b27-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





