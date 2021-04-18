---
description: Die bezeichnete \_ Byte Struktur definiert ein bitpaar mit Bezeichnung. Die Bezeichnung des gekennzeichneten bitpaars wird angezeigt, wenn ein bestimmter Byte-Eigenschafts Wert erkannt wird.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: LABELED_BYTE Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357933"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="6dc1f-104">Bezeichnete \_ Byte Struktur</span><span class="sxs-lookup"><span data-stu-id="6dc1f-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="6dc1f-105">Die **bezeichnete \_ Byte** Struktur definiert ein bitpaar mit Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="6dc1f-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="6dc1f-106">Die **Bezeichnung des gekennzeichneten** bitpaars wird angezeigt, wenn ein bestimmter Byte-Eigenschafts Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6dc1f-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc1f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dc1f-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="6dc1f-108">Member</span><span class="sxs-lookup"><span data-stu-id="6dc1f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6dc1f-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6dc1f-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="6dc1f-110">Der Bytewert der Eigenschaft, die Sie erkennen möchten.</span><span class="sxs-lookup"><span data-stu-id="6dc1f-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="6dc1f-111">**Label**</span><span class="sxs-lookup"><span data-stu-id="6dc1f-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="6dc1f-112">Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene Wert erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6dc1f-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6dc1f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dc1f-113">Remarks</span></span>

<span data-ttu-id="6dc1f-114">Der **lplabeledbytetable** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein **oder mehrere** Bezeichnungs Member der Byte-Wert-Paare definieren.</span><span class="sxs-lookup"><span data-stu-id="6dc1f-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="6dc1f-115">Diese Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten Bytewerts anzeigen möchten, der im Protokoll Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6dc1f-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc1f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dc1f-116">Requirements</span></span>



| <span data-ttu-id="6dc1f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6dc1f-117">Requirement</span></span> | <span data-ttu-id="6dc1f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6dc1f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc1f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6dc1f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc1f-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6dc1f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6dc1f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6dc1f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc1f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6dc1f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6dc1f-123">Header</span><span class="sxs-lookup"><span data-stu-id="6dc1f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dc1f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc1f-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc1f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dc1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc1f-126">SET</span><span class="sxs-lookup"><span data-stu-id="6dc1f-126">SET</span></span>](set.md)
</dt> </dl>

 

 




