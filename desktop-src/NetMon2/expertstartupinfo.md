---
description: Enthält Daten, die einen Experten beschreiben, wenn er gestartet wird.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Expertstartupinfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958727"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="d9d93-103">Expertstartupinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="d9d93-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="d9d93-104">Die Struktur " **expertstartupinfo** " enthält Daten, die einen Experten beschreiben, wenn er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d9d93-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9d93-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="d9d93-106">Member</span><span class="sxs-lookup"><span data-stu-id="d9d93-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d9d93-107">**Flags**</span><span class="sxs-lookup"><span data-stu-id="d9d93-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-108">Flags, die den Experten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d9d93-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-109">**hcapture**</span><span class="sxs-lookup"><span data-stu-id="d9d93-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-110">Handle für eine Erfassung.</span><span class="sxs-lookup"><span data-stu-id="d9d93-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-111">**szcapturefile**</span><span class="sxs-lookup"><span data-stu-id="d9d93-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-112">Der Name der Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="d9d93-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-113">**dwframennummer**</span><span class="sxs-lookup"><span data-stu-id="d9d93-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-114">Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="d9d93-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-115">**hprotocol**</span><span class="sxs-lookup"><span data-stu-id="d9d93-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-116">Handle für das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d9d93-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-117">**lppropertyinst**</span><span class="sxs-lookup"><span data-stu-id="d9d93-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-118">Zeiger auf eine [**propertyinst**](propertyinst.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d9d93-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-119">**sbitfield**</span><span class="sxs-lookup"><span data-stu-id="d9d93-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d93-120">**Bitzahl**</span><span class="sxs-lookup"><span data-stu-id="d9d93-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-121">Wird nur verwendet, wenn der **dataqualifizierermember** der [**propertyinst**](propertyinst.md) -Struktur auf Prop Qual Flags festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d9d93-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="d9d93-122">**Böller**</span><span class="sxs-lookup"><span data-stu-id="d9d93-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="d9d93-123">Wird nur verwendet, wenn der **dataqualifizierermember** der [**propertyinst**](propertyinst.md) -Struktur auf Prop Qual Flags festgelegt ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d9d93-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9d93-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9d93-124">Requirements</span></span>



| <span data-ttu-id="d9d93-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9d93-125">Requirement</span></span> | <span data-ttu-id="d9d93-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d9d93-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d93-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9d93-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d93-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9d93-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d9d93-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9d93-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d93-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9d93-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d9d93-131">Header</span><span class="sxs-lookup"><span data-stu-id="d9d93-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9d93-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9d93-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 




