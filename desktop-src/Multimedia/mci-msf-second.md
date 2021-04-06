---
title: MCI_MSF_SECOND-Makro (mciapi. h)
description: Das MCI \_ MSF \_ Second-Makro ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen über die gepackten Minuten/Sekunden/Frames (MSF) enthält
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858984"
---
# <a name="mci_msf_second-macro"></a><span data-ttu-id="fbfe8-104">MCI \_ MSF- \_ zweites Makro</span><span class="sxs-lookup"><span data-stu-id="fbfe8-104">MCI\_MSF\_SECOND macro</span></span>

<span data-ttu-id="fbfe8-105">Das **MCI \_ MSF \_ Second** -Makro ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen über die gepackten Minuten/Sekunden/Frames (MSF) enthält</span><span class="sxs-lookup"><span data-stu-id="fbfe8-105">The **MCI\_MSF\_SECOND** macro retrieves the seconds component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbfe8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbfe8-106">Syntax</span></span>


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="fbfe8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbfe8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbfe8-108">*dwmsf*</span><span class="sxs-lookup"><span data-stu-id="fbfe8-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="fbfe8-109">Uhrzeit im MSF-Format.</span><span class="sxs-lookup"><span data-stu-id="fbfe8-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbfe8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbfe8-110">Return value</span></span>

<span data-ttu-id="fbfe8-111">Gibt die Sekunden Komponente der angegebenen MSF-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="fbfe8-111">Returns the seconds component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfe8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbfe8-112">Remarks</span></span>

<span data-ttu-id="fbfe8-113">Die Zeit im MSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Minuten enthält, dem nächst bedeutsamen Byte, das Sekunden enthält, und dem nächstniedrigsten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="fbfe8-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="fbfe8-114">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbfe8-114">The most significant byte is unused.</span></span>

<span data-ttu-id="fbfe8-115">Das **MCI \_ MSF \_ Second** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="fbfe8-115">The **MCI\_MSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="fbfe8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbfe8-116">Requirements</span></span>



| <span data-ttu-id="fbfe8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbfe8-117">Requirement</span></span> | <span data-ttu-id="fbfe8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fbfe8-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fbfe8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbfe8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fbfe8-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbfe8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fbfe8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbfe8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fbfe8-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbfe8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fbfe8-123">Header</span><span class="sxs-lookup"><span data-stu-id="fbfe8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbfe8-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbfe8-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbfe8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbfe8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfe8-126">MCI</span><span class="sxs-lookup"><span data-stu-id="fbfe8-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fbfe8-127">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="fbfe8-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





