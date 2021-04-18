---
title: MCI_MSF_MINUTE-Makro (mciapi. h)
description: Das MCI- \_ MSF \_ -Minute-Makro ruft die Minuten Komponente von einem Parameter ab, der die Informationen zu den Informationen über die gepackten Minuten/Sekunden/Frames (MSF
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344105"
---
# <a name="mci_msf_minute-macro"></a><span data-ttu-id="c3466-104">MCI- \_ MSF- \_ Minute-Makro</span><span class="sxs-lookup"><span data-stu-id="c3466-104">MCI\_MSF\_MINUTE macro</span></span>

<span data-ttu-id="c3466-105">Das **MCI- \_ MSF- \_ Minute** -Makro ruft die Minuten Komponente von einem Parameter ab, der die Informationen zu den Informationen über die gepackten Minuten/Sekunden/Frames (MSF</span><span class="sxs-lookup"><span data-stu-id="c3466-105">The **MCI\_MSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3466-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3466-106">Syntax</span></span>


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="c3466-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3466-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3466-108">*dwmsf*</span><span class="sxs-lookup"><span data-stu-id="c3466-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="c3466-109">Uhrzeit im MSF-Format.</span><span class="sxs-lookup"><span data-stu-id="c3466-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3466-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3466-110">Return value</span></span>

<span data-ttu-id="c3466-111">Gibt die Minuten Komponente der angegebenen MSF-Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="c3466-111">Returns the minutes component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3466-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3466-112">Remarks</span></span>

<span data-ttu-id="c3466-113">Die Zeit im MSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Minuten enthält, dem nächst bedeutsamen Byte, das Sekunden enthält, und dem nächstniedrigsten Byte mit Frames ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c3466-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="c3466-114">Das signifikanteste Byte wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3466-114">The most significant byte is unused.</span></span>

<span data-ttu-id="c3466-115">Das **MCI \_ MSF \_ Minute** -Makro wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="c3466-115">The **MCI\_MSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a><span data-ttu-id="c3466-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3466-116">Requirements</span></span>



| <span data-ttu-id="c3466-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3466-117">Requirement</span></span> | <span data-ttu-id="c3466-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c3466-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c3466-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3466-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3466-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3466-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c3466-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3466-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3466-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3466-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c3466-123">Header</span><span class="sxs-lookup"><span data-stu-id="c3466-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3466-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3466-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3466-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3466-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3466-126">MCI</span><span class="sxs-lookup"><span data-stu-id="c3466-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c3466-127">MCI-Makros</span><span class="sxs-lookup"><span data-stu-id="c3466-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





