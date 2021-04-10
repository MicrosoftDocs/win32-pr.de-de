---
description: 'Weitere Informationen zu: etweventwrite-Funktion'
title: Etweventwrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041480"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="50117-103">Etweventwrite-Funktion</span><span class="sxs-lookup"><span data-stu-id="50117-103">EtwEventWrite function</span></span>

<span data-ttu-id="50117-104">[Die etweventwrite-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.]</span><span class="sxs-lookup"><span data-stu-id="50117-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="50117-105">Schreibt ein Basisereignis in eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="50117-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="50117-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="50117-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="50117-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="50117-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50117-108">*Reghandle*</span><span class="sxs-lookup"><span data-stu-id="50117-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="50117-109">Reghandle für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="50117-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="50117-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="50117-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="50117-111">Der Ereignis Deskriptor des Ereignisses, das protokolliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="50117-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="50117-112">*Userdatacount*</span><span class="sxs-lookup"><span data-stu-id="50117-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="50117-113">Anzahl von Benutzerdaten Elementen.</span><span class="sxs-lookup"><span data-stu-id="50117-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="50117-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="50117-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="50117-115">Zeiger auf ein Array von Benutzerdaten Elementen.</span><span class="sxs-lookup"><span data-stu-id="50117-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50117-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50117-116">Return value</span></span>

<span data-ttu-id="50117-117">Ein Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="50117-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="50117-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50117-118">Remarks</span></span>

<span data-ttu-id="50117-119">Die etweventwrite-Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.</span><span class="sxs-lookup"><span data-stu-id="50117-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="50117-120">Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen öffentliche Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="50117-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="50117-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50117-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="50117-122">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="50117-122">**Target Platform**</span></span> | <span data-ttu-id="50117-123">Windows</span><span class="sxs-lookup"><span data-stu-id="50117-123">Windows</span></span> |
| <span data-ttu-id="50117-124">**Header**</span><span class="sxs-lookup"><span data-stu-id="50117-124">**Header**</span></span> | <span data-ttu-id="50117-125">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="50117-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="50117-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50117-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50117-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="50117-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="50117-128">EventWrite-Ex</span><span class="sxs-lookup"><span data-stu-id="50117-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
