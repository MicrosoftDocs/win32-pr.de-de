---
description: Die macframe-Struktur ist eine Vereinigung der gängigsten anfänglichen Protokolle.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Macframe-Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357368"
---
# <a name="macframe-union"></a><span data-ttu-id="8321b-103">Macframe-Union</span><span class="sxs-lookup"><span data-stu-id="8321b-103">MACFRAME union</span></span>

<span data-ttu-id="8321b-104">Die **macframe** -Struktur ist eine Vereinigung der gängigsten anfänglichen Protokolle.</span><span class="sxs-lookup"><span data-stu-id="8321b-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="8321b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8321b-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="8321b-106">Member</span><span class="sxs-lookup"><span data-stu-id="8321b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8321b-107">**Machereader**</span><span class="sxs-lookup"><span data-stu-id="8321b-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="8321b-108">Generischer Zeiger auf einen Frame.</span><span class="sxs-lookup"><span data-stu-id="8321b-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="8321b-109">**Ethernet**</span><span class="sxs-lookup"><span data-stu-id="8321b-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="8321b-110">Ethernet-Zeiger auf einen Frame.</span><span class="sxs-lookup"><span data-stu-id="8321b-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="8321b-111">**Tokenring**</span><span class="sxs-lookup"><span data-stu-id="8321b-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="8321b-112">Tokenringzeiger auf einen Frame.</span><span class="sxs-lookup"><span data-stu-id="8321b-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="8321b-113">**FDDI**</span><span class="sxs-lookup"><span data-stu-id="8321b-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="8321b-114">FDDI-Zeiger auf einen Frame.</span><span class="sxs-lookup"><span data-stu-id="8321b-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8321b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8321b-115">Remarks</span></span>

<span data-ttu-id="8321b-116">Diese Struktur wird am häufigsten als Überlagerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8321b-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="8321b-117">Um die Eigenschaften des ersten Protokolls zugänglich zu machen, wandeln Sie den Frame in denselben Typ wie das Protokoll um.</span><span class="sxs-lookup"><span data-stu-id="8321b-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="8321b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8321b-118">Requirements</span></span>



| <span data-ttu-id="8321b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8321b-119">Requirement</span></span> | <span data-ttu-id="8321b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8321b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8321b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8321b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8321b-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8321b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8321b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8321b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8321b-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8321b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8321b-125">Header</span><span class="sxs-lookup"><span data-stu-id="8321b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8321b-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8321b-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




