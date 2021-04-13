---
description: Die Struktur von "expertframedescriptor" enthält Informationen zu einem Frame. Wenn der Experte die Funktion "expertgetframe" erfolgreich aufruft, übergibt Netzwerkmonitor die "expertframedescriptor"-Struktur an den Experten zurück.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Struktur von "expertframedescriptor" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484339"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="eb214-104">Struktur von "expertframedescriptor"</span><span class="sxs-lookup"><span data-stu-id="eb214-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="eb214-105">Die Struktur von " **expertframedescriptor** " enthält Informationen zu einem Frame.</span><span class="sxs-lookup"><span data-stu-id="eb214-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="eb214-106">Wenn der Experte die Funktion " [**expertgetframe**](expertgetframe.md) " erfolgreich aufruft, übergibt Netzwerkmonitor die " **expertframedescriptor** "-Struktur an den Experten zurück.</span><span class="sxs-lookup"><span data-stu-id="eb214-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb214-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb214-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="eb214-108">Member</span><span class="sxs-lookup"><span data-stu-id="eb214-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb214-109">**Framezahl**</span><span class="sxs-lookup"><span data-stu-id="eb214-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="eb214-110">Die Nummer eines angegebenen Frames.</span><span class="sxs-lookup"><span data-stu-id="eb214-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="eb214-111">**hframe**</span><span class="sxs-lookup"><span data-stu-id="eb214-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="eb214-112">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="eb214-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="eb214-113">**pFrame**</span><span class="sxs-lookup"><span data-stu-id="eb214-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="eb214-114">Zeiger auf einen rohframe.</span><span class="sxs-lookup"><span data-stu-id="eb214-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="eb214-115">**lprecognizedatabel**</span><span class="sxs-lookup"><span data-stu-id="eb214-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="eb214-116">Tabelle, die angibt, wo jeder Parser den Anfang der Daten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="eb214-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="eb214-117">**lppropertytable**</span><span class="sxs-lookup"><span data-stu-id="eb214-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="eb214-118">Tabelle mit Frame Eigenschaften, die vom Parser identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="eb214-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb214-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb214-119">Remarks</span></span>

<span data-ttu-id="eb214-120">Wenn der Experte \_ beim Aufrufen von " \_ [**expertgetframe**](expertgetframe.md)" Flags anfügen-Eigenschaften angibt, ist das **szpropertytext** -Element in jeder [**propertyinst**](propertyinst.md) -Struktur **null**.</span><span class="sxs-lookup"><span data-stu-id="eb214-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="eb214-121">Wenn der Experte \_ beim Aufrufen der Funktion "-Funktion" keine Flags anfügen- \_ Eigenschaften angibt, ist das **lppropertytable** -Element bei Rückgabe **null** . [](expertgetframe.md)</span><span class="sxs-lookup"><span data-stu-id="eb214-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb214-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb214-122">Requirements</span></span>



| <span data-ttu-id="eb214-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb214-123">Requirement</span></span> | <span data-ttu-id="eb214-124">Wert</span><span class="sxs-lookup"><span data-stu-id="eb214-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eb214-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb214-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eb214-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb214-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eb214-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb214-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eb214-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb214-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eb214-129">Header</span><span class="sxs-lookup"><span data-stu-id="eb214-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb214-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb214-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 




