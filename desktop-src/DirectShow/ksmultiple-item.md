---
description: Die ksmultiple \_ -Elementstruktur beschreibt die Größe und die Anzahl der Eigenschaften variabler Länge in den kernelmoduspins.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM Struktur (". h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361366"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="3575f-103">Ksmultiple- \_ Elementstruktur</span><span class="sxs-lookup"><span data-stu-id="3575f-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="3575f-104">Die `KSMULTIPLE_ITEM` -Struktur beschreibt die Größe und die Anzahl der Eigenschaften variabler Länge in den kernelmoduspins.</span><span class="sxs-lookup"><span data-stu-id="3575f-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="3575f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3575f-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="3575f-106">Member</span><span class="sxs-lookup"><span data-stu-id="3575f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3575f-107">**Größe**</span><span class="sxs-lookup"><span data-stu-id="3575f-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3575f-108">Größe des zurückgegebenen Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3575f-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="3575f-109">Die Größe schließt die **ksmultiple- \_ Element** Struktur und die folgenden Elemente ein.</span><span class="sxs-lookup"><span data-stu-id="3575f-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="3575f-110">**Count**</span><span class="sxs-lookup"><span data-stu-id="3575f-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="3575f-111">Gibt die Gesamtzahl der Elemente an, die dieser Struktur folgen.</span><span class="sxs-lookup"><span data-stu-id="3575f-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3575f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3575f-112">Requirements</span></span>



| <span data-ttu-id="3575f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3575f-113">Requirement</span></span> | <span data-ttu-id="3575f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3575f-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3575f-115">Header</span><span class="sxs-lookup"><span data-stu-id="3575f-115">Header</span></span><br/> | <dl> <span data-ttu-id="3575f-116"><dt>. H.</dt></span><span class="sxs-lookup"><span data-stu-id="3575f-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3575f-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3575f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3575f-118">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3575f-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="3575f-119">**Ikspin:: ksquerymediums**</span><span class="sxs-lookup"><span data-stu-id="3575f-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="3575f-120">**Regpinmedium**</span><span class="sxs-lookup"><span data-stu-id="3575f-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




