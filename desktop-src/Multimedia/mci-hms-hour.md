---
title: MCI_HMS_HOUR-Makro (mciapi. h)
description: Das MCI \_ - \_ Element "HMS Hour" Ruft die Stunden Komponente von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040987"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="927e5-104">MCI- \_ HMS- \_ Stunden-Makro</span><span class="sxs-lookup"><span data-stu-id="927e5-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="927e5-105">Das **MCI-Element " \_ HMS \_ Hour** " Ruft die Stunden Komponente von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.</span><span class="sxs-lookup"><span data-stu-id="927e5-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="927e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="927e5-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="927e5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="927e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="927e5-108">*dwhms*</span><span class="sxs-lookup"><span data-stu-id="927e5-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="927e5-109">Zeit im "HMS"-Format.</span><span class="sxs-lookup"><span data-stu-id="927e5-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="927e5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="927e5-110">Return value</span></span>

<span data-ttu-id="927e5-111">Gibt die Stunden Komponente der angegebenen HMS-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="927e5-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="927e5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="927e5-112">Remarks</span></span>

<span data-ttu-id="927e5-113">Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="927e5-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="927e5-114">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="927e5-114">The most significant byte is unused.</span></span>

<span data-ttu-id="927e5-115">Das **MCI-Element " \_ HMS \_ Hour** " ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="927e5-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="927e5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="927e5-116">Requirements</span></span>



| <span data-ttu-id="927e5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="927e5-117">Requirement</span></span> | <span data-ttu-id="927e5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="927e5-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="927e5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="927e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="927e5-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="927e5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="927e5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="927e5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="927e5-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="927e5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="927e5-123">Header</span><span class="sxs-lookup"><span data-stu-id="927e5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="927e5-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="927e5-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927e5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="927e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927e5-126">MCI</span><span class="sxs-lookup"><span data-stu-id="927e5-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="927e5-127">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="927e5-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





