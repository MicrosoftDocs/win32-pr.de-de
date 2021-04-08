---
description: Die getcapturemactype-Funktion gibt den Mac-Typ einer angegebenen Erfassung zurück.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Getcapturemactype-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750096"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="3d858-103">Getcapturemactype-Funktion</span><span class="sxs-lookup"><span data-stu-id="3d858-103">GetCaptureMacType function</span></span>

<span data-ttu-id="3d858-104">Die **getcapturemactype** -Funktion gibt den Mac-Typ einer angegebenen Erfassung zurück.</span><span class="sxs-lookup"><span data-stu-id="3d858-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d858-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d858-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="3d858-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d858-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d858-107">*hcapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d858-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d858-108">Handle für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="3d858-108">Handle to the capture.</span></span> <span data-ttu-id="3d858-109">Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **getcapturemactype** .</span><span class="sxs-lookup"><span data-stu-id="3d858-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d858-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d858-110">Return value</span></span>

<span data-ttu-id="3d858-111">Wenn die Funktion erfolgreich ist, ist der Rückgabewert einer der folgenden Mac-Typen.</span><span class="sxs-lookup"><span data-stu-id="3d858-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="3d858-112">Unbekannter Mac- \_ Typ. \_</span><span class="sxs-lookup"><span data-stu-id="3d858-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="3d858-113">Mac- \_ Typ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="3d858-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="3d858-114">Mac- \_ Typ \_ TokenRing</span><span class="sxs-lookup"><span data-stu-id="3d858-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="3d858-115">Mac- \_ Typ " \_ f"</span><span class="sxs-lookup"><span data-stu-id="3d858-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="3d858-116">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3d858-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="3d858-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3d858-117">Return code</span></span>                                                                                              | <span data-ttu-id="3d858-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d858-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="3d858-119"><dt>**nmerr- \_ Mac- \_ Typ \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="3d858-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="3d858-120">Ein bekannter Mac-Typ konnte von Netzwerkmonitor nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="3d858-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d858-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d858-121">Remarks</span></span>

<span data-ttu-id="3d858-122">Das Handle der Erfassung kann auf verschiedene Weise abgerufen werden, abhängig von der Person, die den-Befehl aufruft.</span><span class="sxs-lookup"><span data-stu-id="3d858-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="3d858-123">Für Experten wird das Handle im **hcapture** -Member der " [expertstartupinfo](expertstartupinfo.md) "-Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="3d858-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="3d858-124">Für Parser kann das Erfassungs Handle abgerufen werden, indem die [getframecapturehandle](getframecapturehandle.md) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3d858-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="3d858-125">[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturemactype** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3d858-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d858-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d858-126">Requirements</span></span>



| <span data-ttu-id="3d858-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d858-127">Requirement</span></span> | <span data-ttu-id="3d858-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3d858-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3d858-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d858-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3d858-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d858-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3d858-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d858-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3d858-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d858-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3d858-133">Header</span><span class="sxs-lookup"><span data-stu-id="3d858-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d858-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d858-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3d858-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d858-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d858-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d858-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d858-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3d858-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d858-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d858-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




