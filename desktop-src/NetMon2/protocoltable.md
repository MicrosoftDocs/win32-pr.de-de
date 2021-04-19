---
description: Die protocoltable-Struktur enthält eine Liste von Protokollen.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Protocoltable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373192"
---
# <a name="protocoltable-structure"></a><span data-ttu-id="c0d6a-103">Protocoltable-Struktur</span><span class="sxs-lookup"><span data-stu-id="c0d6a-103">PROTOCOLTABLE structure</span></span>

<span data-ttu-id="c0d6a-104">Die **protocoltable** -Struktur enthält eine Liste von Protokollen.</span><span class="sxs-lookup"><span data-stu-id="c0d6a-104">The **PROTOCOLTABLE** structure contains a list of protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d6a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0d6a-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a><span data-ttu-id="c0d6a-106">Member</span><span class="sxs-lookup"><span data-stu-id="c0d6a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0d6a-107">**nprotokolle**</span><span class="sxs-lookup"><span data-stu-id="c0d6a-107">**nProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c0d6a-108">Anzahl der aktivierten Protokolle.</span><span class="sxs-lookup"><span data-stu-id="c0d6a-108">Number of protocols that are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="c0d6a-109">**hprotocol**</span><span class="sxs-lookup"><span data-stu-id="c0d6a-109">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="c0d6a-110">Array von Handles für aktivierte Protokolle.</span><span class="sxs-lookup"><span data-stu-id="c0d6a-110">Array of handles to enabled protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0d6a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0d6a-111">Requirements</span></span>



| <span data-ttu-id="c0d6a-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0d6a-112">Requirement</span></span> | <span data-ttu-id="c0d6a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d6a-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d6a-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0d6a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d6a-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0d6a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c0d6a-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0d6a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d6a-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0d6a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0d6a-118">Header</span><span class="sxs-lookup"><span data-stu-id="c0d6a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0d6a-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0d6a-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




