---
title: MCI_TMSF_SECOND-Makro (mciapi. h)
description: Das zweite MCI \_ TMSF- \_ Makro ruft die Sekunden Komponente von einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF) enthält.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104007"
---
# <a name="mci_tmsf_second-macro"></a><span data-ttu-id="f94f1-104">Zweites MCI \_ TMSF- \_ Makro</span><span class="sxs-lookup"><span data-stu-id="f94f1-104">MCI\_TMSF\_SECOND macro</span></span>

<span data-ttu-id="f94f1-105">Das **\_ \_ zweite MCI TMSF** -Makro ruft die Sekunden Komponente von einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF) enthält.</span><span class="sxs-lookup"><span data-stu-id="f94f1-105">The **MCI\_TMSF\_SECOND** macro retrieves the seconds component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94f1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f94f1-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="f94f1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f94f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94f1-108">*dwtmsf*</span><span class="sxs-lookup"><span data-stu-id="f94f1-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="f94f1-109">Zeit im TMSF-Format.</span><span class="sxs-lookup"><span data-stu-id="f94f1-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94f1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f94f1-110">Return value</span></span>

<span data-ttu-id="f94f1-111">Gibt die Sekunden Komponente der angegebenen TMSF-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="f94f1-111">Returns the seconds component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="f94f1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f94f1-112">Remarks</span></span>

<span data-ttu-id="f94f1-113">Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="f94f1-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="f94f1-114">Das **\_ \_ zweite MCI TMSF** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f94f1-114">The **MCI\_TMSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="f94f1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f94f1-115">Requirements</span></span>



| <span data-ttu-id="f94f1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f94f1-116">Requirement</span></span> | <span data-ttu-id="f94f1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f94f1-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f94f1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f94f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f94f1-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f94f1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f94f1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f94f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f94f1-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f94f1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f94f1-122">Header</span><span class="sxs-lookup"><span data-stu-id="f94f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f94f1-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94f1-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94f1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f94f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94f1-125">MCI</span><span class="sxs-lookup"><span data-stu-id="f94f1-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f94f1-126">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="f94f1-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





