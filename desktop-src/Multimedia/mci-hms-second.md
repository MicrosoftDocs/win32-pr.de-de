---
title: MCI_HMS_SECOND-Makro (mciapi. h)
description: Das MCI-Element für die \_ HMS \_ -Sekunde ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen zu den gepackten Stunden/Minuten/Sekunden (
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859273"
---
# <a name="mci_hms_second-macro"></a><span data-ttu-id="c6095-104">MCI- \_ HMS- \_ zweites Makro</span><span class="sxs-lookup"><span data-stu-id="c6095-104">MCI\_HMS\_SECOND macro</span></span>

<span data-ttu-id="c6095-105">Das MCI-Element für die **\_ HMS- \_ Sekunde** Ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen zu den gepackten Stunden/Minuten/Sekunden (</span><span class="sxs-lookup"><span data-stu-id="c6095-105">The **MCI\_HMS\_SECOND** macro retrieves the seconds component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6095-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6095-106">Syntax</span></span>


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="c6095-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6095-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6095-108">*dwhms*</span><span class="sxs-lookup"><span data-stu-id="c6095-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="c6095-109">Zeit im "HMS"-Format.</span><span class="sxs-lookup"><span data-stu-id="c6095-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6095-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6095-110">Return value</span></span>

<span data-ttu-id="c6095-111">Gibt die Sekunden Komponente der angegebenen HMS-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="c6095-111">Returns the seconds component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6095-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6095-112">Remarks</span></span>

<span data-ttu-id="c6095-113">Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c6095-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="c6095-114">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6095-114">The most significant byte is unused.</span></span>

<span data-ttu-id="c6095-115">Das **MCI-Element " \_ HMS \_ Second** " ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c6095-115">The **MCI\_HMS\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="c6095-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6095-116">Requirements</span></span>



| <span data-ttu-id="c6095-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6095-117">Requirement</span></span> | <span data-ttu-id="c6095-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c6095-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6095-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6095-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6095-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6095-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c6095-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6095-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6095-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6095-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c6095-123">Header</span><span class="sxs-lookup"><span data-stu-id="c6095-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6095-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6095-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6095-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6095-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6095-126">MCI</span><span class="sxs-lookup"><span data-stu-id="c6095-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c6095-127">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="c6095-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





