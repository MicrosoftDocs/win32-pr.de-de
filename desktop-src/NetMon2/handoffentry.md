---
description: Die handoffentry-Struktur definiert einen bestimmten Protokolleintrag in einer handofftable-Struktur.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Handoffentry-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525127"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="5ee8b-103">Handoffentry-Struktur</span><span class="sxs-lookup"><span data-stu-id="5ee8b-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="5ee8b-104">Die **handoffentry** -Struktur definiert einen bestimmten Protokolleintrag in einer **handofftable** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="5ee8b-105">Diese Struktur wird von Netzwerkmonitor basierend auf Informationen in einer vom Benutzer bereitgestellten ini-Datei ausgefüllt, die beim Aufrufen der [**createhandofftable**](createhandofftable.md) -Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="5ee8b-106">Diese Struktur sollte nie explizit von einer Anwendung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee8b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ee8b-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="5ee8b-108">Member</span><span class="sxs-lookup"><span data-stu-id="5ee8b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ee8b-109">**Hacke \_ sig**</span><span class="sxs-lookup"><span data-stu-id="5ee8b-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="5ee8b-110">Die Signatur, die diesen Eintrag als einen Übergabe Tabelleneintrag bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="5ee8b-111">**Hacke- \_ protidentnumber**</span><span class="sxs-lookup"><span data-stu-id="5ee8b-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5ee8b-112">Von der vom Benutzer bereitgestellte ini-Datei bereitgestellte Protokollnummer.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="5ee8b-113">**Hacken- \_ protocolhandle**</span><span class="sxs-lookup"><span data-stu-id="5ee8b-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="5ee8b-114">Protokoll handle, das mithilfe des Protokoll namens erstellt wird, der von der vom Benutzer bereitgestellten ini-Datei bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="5ee8b-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="5ee8b-115">**\_protocoldata hacken**</span><span class="sxs-lookup"><span data-stu-id="5ee8b-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="5ee8b-116">Protokollinstanzdaten, die von der vom Benutzer bereitgestellten ini-Datei</span><span class="sxs-lookup"><span data-stu-id="5ee8b-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ee8b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ee8b-117">Remarks</span></span>

<span data-ttu-id="5ee8b-118">Diese Struktur wird von Netzwerkmonitor ausgefüllt, wenn Netzwerkmonitor eine Übergabe Tabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee8b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ee8b-119">Requirements</span></span>



| <span data-ttu-id="5ee8b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ee8b-120">Requirement</span></span> | <span data-ttu-id="5ee8b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5ee8b-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee8b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ee8b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee8b-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ee8b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5ee8b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ee8b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee8b-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ee8b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5ee8b-126">Header</span><span class="sxs-lookup"><span data-stu-id="5ee8b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ee8b-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee8b-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ee8b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ee8b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee8b-129">Handofftable</span><span class="sxs-lookup"><span data-stu-id="5ee8b-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




