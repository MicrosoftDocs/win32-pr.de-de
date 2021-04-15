---
description: Gibt den aktuellen Status eines laufenden Experten an.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Expertenstatus-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525157"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="bb745-103">Expertenstatus-Struktur</span><span class="sxs-lookup"><span data-stu-id="bb745-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="bb745-104">Die Struktur " **Expertenstatus** " gibt den aktuellen Status eines laufenden Experten an.</span><span class="sxs-lookup"><span data-stu-id="bb745-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb745-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb745-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="bb745-106">Member</span><span class="sxs-lookup"><span data-stu-id="bb745-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb745-107">**Status**</span><span class="sxs-lookup"><span data-stu-id="bb745-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="bb745-108">Aktueller von der [**expertstatusenumeration**](expertstatusenumeration.md) -Enumeration definierter Wert des Expertenstatus.</span><span class="sxs-lookup"><span data-stu-id="bb745-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="bb745-109">**Unter Status**</span><span class="sxs-lookup"><span data-stu-id="bb745-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="bb745-110">Unter Statuswert.</span><span class="sxs-lookup"><span data-stu-id="bb745-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="bb745-111">**Prozentuabgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="bb745-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="bb745-112">Prozentualer Abschluss der Expertenanalyse von Netzwerkdaten.</span><span class="sxs-lookup"><span data-stu-id="bb745-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="bb745-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="bb745-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="bb745-114">Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="bb745-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="bb745-115">**szStatusText**</span><span class="sxs-lookup"><span data-stu-id="bb745-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="bb745-116">Text, der den Expertenstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bb745-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb745-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb745-117">Requirements</span></span>



| <span data-ttu-id="bb745-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb745-118">Requirement</span></span> | <span data-ttu-id="bb745-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bb745-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb745-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb745-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb745-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb745-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb745-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb745-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb745-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb745-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bb745-124">Header</span><span class="sxs-lookup"><span data-stu-id="bb745-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb745-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb745-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




