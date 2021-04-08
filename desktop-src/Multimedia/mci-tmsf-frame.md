---
title: MCI_TMSF_FRAME-Makro (mciapi. h)
description: Das MCI \_ TMSF- \_ Frame-Makro ruft die Frames-Komponente von einem Parameter ab, der gepackte Titel/Minuten/Sekunden/Frames (TMSF) enthält.
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740256"
---
# <a name="mci_tmsf_frame-macro"></a><span data-ttu-id="5058d-104">MCI \_ TMSF- \_ Frame-Makro</span><span class="sxs-lookup"><span data-stu-id="5058d-104">MCI\_TMSF\_FRAME macro</span></span>

<span data-ttu-id="5058d-105">Das **MCI \_ TMSF- \_ Frame** -Makro ruft die Frames-Komponente von einem Parameter ab, der gepackte Titel/Minuten/Sekunden/Frames (TMSF) enthält.</span><span class="sxs-lookup"><span data-stu-id="5058d-105">The **MCI\_TMSF\_FRAME** macro retrieves the frames component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5058d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5058d-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="5058d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5058d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5058d-108">*dwtmsf*</span><span class="sxs-lookup"><span data-stu-id="5058d-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="5058d-109">Zeit im TMSF-Format.</span><span class="sxs-lookup"><span data-stu-id="5058d-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5058d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5058d-110">Return value</span></span>

<span data-ttu-id="5058d-111">Gibt die Frames-Komponente der angegebenen TMSF-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="5058d-111">Returns the frames component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="5058d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5058d-112">Remarks</span></span>

<span data-ttu-id="5058d-113">Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="5058d-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="5058d-114">Das **MCI \_ TMSF- \_ Frame** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="5058d-114">The **MCI\_TMSF\_FRAME** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a><span data-ttu-id="5058d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5058d-115">Requirements</span></span>



| <span data-ttu-id="5058d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5058d-116">Requirement</span></span> | <span data-ttu-id="5058d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5058d-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5058d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5058d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5058d-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5058d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5058d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5058d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5058d-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5058d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5058d-122">Header</span><span class="sxs-lookup"><span data-stu-id="5058d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5058d-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5058d-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5058d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5058d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5058d-125">MCI</span><span class="sxs-lookup"><span data-stu-id="5058d-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5058d-126">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="5058d-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





