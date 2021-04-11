---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: Das Format der cfstr \_ DSOP \_ DS- \_ Auswahlliste in der \_ Zwischenablage bietet einen HGLOBAL, der eine DS- \_ Auswahl \_ Listenstruktur enthält. Die Struktur der DS- \_ Auswahl \_ Liste enthält Daten zu den Elementen, die im Dialogfeld Verzeichnis Objektauswahl ausgewählt wurden.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949717"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="ad2cd-104">cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste</span><span class="sxs-lookup"><span data-stu-id="ad2cd-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="ad2cd-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="ad2cd-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad2cd-106">"cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste"</span><span class="sxs-lookup"><span data-stu-id="ad2cd-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="ad2cd-107">Das Zwischenablage Format der **cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste** wird durch das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) bereitgestellt, das durch Aufrufen von [**idsobjectpicker:: invokedialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ad2cd-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="ad2cd-108">Das Format der **cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste** in der Zwischenablage bietet einen **HGLOBAL** , der eine [**DS- \_ Auswahl \_ Listen**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="ad2cd-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="ad2cd-109">Die Struktur der **DS- \_ Auswahl \_ Liste** enthält Daten zu den Elementen, die im Dialogfeld [Verzeichnis Objekt](directory-object-picker.md) Auswahl ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="ad2cd-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad2cd-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad2cd-110">Requirements</span></span>



| <span data-ttu-id="ad2cd-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad2cd-111">Requirement</span></span> | <span data-ttu-id="ad2cd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ad2cd-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2cd-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad2cd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ad2cd-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad2cd-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="ad2cd-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad2cd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ad2cd-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad2cd-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="ad2cd-117">Header</span><span class="sxs-lookup"><span data-stu-id="ad2cd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad2cd-118"><dt>Objsel. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad2cd-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad2cd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad2cd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad2cd-120">**DS- \_ Auswahl \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="ad2cd-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="ad2cd-121">**Idsobjectpicker:: invokedialog**</span><span class="sxs-lookup"><span data-stu-id="ad2cd-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="ad2cd-122">Verzeichnis Objektauswahl</span><span class="sxs-lookup"><span data-stu-id="ad2cd-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

