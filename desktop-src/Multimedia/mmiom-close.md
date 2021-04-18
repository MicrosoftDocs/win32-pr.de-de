---
title: MMIOM_CLOSE Meldung (MMSYSTEM. h)
description: Die mmiom \_ Close-Nachricht wird von der mmioclose-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geschlossen wird.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519295"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="59e7d-104">Mmiom- \_ Meldung schließen</span><span class="sxs-lookup"><span data-stu-id="59e7d-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="59e7d-105">Die **mmiom \_ Close** -Nachricht wird von der [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine Datei geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="59e7d-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="59e7d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59e7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e7d-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lcloseflags*</span><span class="sxs-lookup"><span data-stu-id="59e7d-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="59e7d-108">Flags, die im **wFlags**-Parameter von **mmioclose** enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="59e7d-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e7d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59e7d-109">Return Value</span></span>

<span data-ttu-id="59e7d-110">Gibt 0 (null) zurück, wenn die Datei erfolgreich geschlossen wurde, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="59e7d-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e7d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59e7d-111">Requirements</span></span>



| <span data-ttu-id="59e7d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59e7d-112">Requirement</span></span> | <span data-ttu-id="59e7d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="59e7d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e7d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59e7d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="59e7d-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59e7d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59e7d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59e7d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="59e7d-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59e7d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59e7d-118">Header</span><span class="sxs-lookup"><span data-stu-id="59e7d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="59e7d-119"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59e7d-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

