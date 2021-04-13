---
title: MCI_TMSF_MINUTE-Makro (mciapi. h)
description: Das MCI \_ TMSF \_ Minute-Makro ruft die Minuten Komponente von einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF) enthält.
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- MCI_TMSF_MINUTE Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517816"
---
# <a name="mci_tmsf_minute-macro"></a><span data-ttu-id="c6d8b-104">MCI \_ TMSF- \_ Minuten Makro</span><span class="sxs-lookup"><span data-stu-id="c6d8b-104">MCI\_TMSF\_MINUTE macro</span></span>

<span data-ttu-id="c6d8b-105">Das **MCI \_ TMSF \_ Minute** -Makro ruft die Minuten Komponente von einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF) enthält.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-105">The **MCI\_TMSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d8b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6d8b-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_MINUTE(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="c6d8b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6d8b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d8b-108">*dwtmsf*</span><span class="sxs-lookup"><span data-stu-id="c6d8b-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d8b-109">Zeit im TMSF-Format.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6d8b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6d8b-110">Return value</span></span>

<span data-ttu-id="c6d8b-111">Gibt die Minuten Komponente der angegebenen TMSF-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-111">Returns the minutes component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6d8b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6d8b-112">Remarks</span></span>

<span data-ttu-id="c6d8b-113">Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c6d8b-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="c6d8b-114">Das **MCI \_ TMSF \_ Minute** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c6d8b-114">The **MCI\_TMSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="c6d8b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6d8b-115">Requirements</span></span>



| <span data-ttu-id="c6d8b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6d8b-116">Requirement</span></span> | <span data-ttu-id="c6d8b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c6d8b-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d8b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6d8b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d8b-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6d8b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c6d8b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6d8b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d8b-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6d8b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c6d8b-122">Header</span><span class="sxs-lookup"><span data-stu-id="c6d8b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d8b-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6d8b-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d8b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6d8b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d8b-125">MCI</span><span class="sxs-lookup"><span data-stu-id="c6d8b-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c6d8b-126">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="c6d8b-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





