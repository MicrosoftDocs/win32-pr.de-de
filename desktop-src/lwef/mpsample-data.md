---
title: MPSAMPLE_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten, die an die Rückruffunktion der Beispiel Übermittlung übergeben werden.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSAMPLE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106298"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="1fd7c-105">Mpsample- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="1fd7c-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="1fd7c-106">Benachrichtigungs Daten, die an die Rückruffunktion der Beispiel Übermittlung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd7c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fd7c-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="1fd7c-108">Member</span><span class="sxs-lookup"><span data-stu-id="1fd7c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fd7c-109">**dwsampleingedex**</span><span class="sxs-lookup"><span data-stu-id="1fd7c-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="1fd7c-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1fd7c-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1fd7c-111">Der Index des Beispiel Elements, für das der Übermittlungs Status gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="1fd7c-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fd7c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fd7c-112">Requirements</span></span>



| <span data-ttu-id="1fd7c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fd7c-113">Requirement</span></span> | <span data-ttu-id="1fd7c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1fd7c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd7c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fd7c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd7c-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fd7c-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1fd7c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fd7c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd7c-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fd7c-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fd7c-119">Header</span><span class="sxs-lookup"><span data-stu-id="1fd7c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fd7c-120"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fd7c-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





