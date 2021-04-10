---
title: MCI_HMS_MINUTE-Makro (mciapi. h)
description: Das MCI \_ - \_ Element "HMS Minute" Ruft die Komponente "Minutes" von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106209"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="9fc1e-104">MCI-nach-oben- \_ \_ Makro</span><span class="sxs-lookup"><span data-stu-id="9fc1e-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="9fc1e-105">Das **MCI-Element " \_ HMS \_ Minute** " Ruft die Komponente "Minutes" von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc1e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fc1e-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="9fc1e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fc1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc1e-108">*dwhms*</span><span class="sxs-lookup"><span data-stu-id="9fc1e-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc1e-109">Zeit im "HMS"-Format.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc1e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fc1e-110">Return value</span></span>

<span data-ttu-id="9fc1e-111">Gibt die Minuten Komponente der angegebenen HMS-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc1e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fc1e-112">Remarks</span></span>

<span data-ttu-id="9fc1e-113">Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="9fc1e-114">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fc1e-114">The most significant byte is unused.</span></span>

<span data-ttu-id="9fc1e-115">Das **MCI-Element " \_ HMS \_ Minute** " ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="9fc1e-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="9fc1e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fc1e-116">Requirements</span></span>



| <span data-ttu-id="9fc1e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fc1e-117">Requirement</span></span> | <span data-ttu-id="9fc1e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9fc1e-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc1e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fc1e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc1e-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fc1e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9fc1e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fc1e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc1e-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fc1e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9fc1e-123">Header</span><span class="sxs-lookup"><span data-stu-id="9fc1e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc1e-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc1e-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc1e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fc1e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc1e-126">MCI</span><span class="sxs-lookup"><span data-stu-id="9fc1e-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9fc1e-127">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="9fc1e-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





