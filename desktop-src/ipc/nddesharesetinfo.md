---
description: Legt DDE-Freigabe Informationen fest. Dies erfolgt in der Regel nach der Bearbeitung.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Nddesharesetinfo-Funktion (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339736"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="e1b8a-104">Nddesharesetinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1b8a-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="e1b8a-105">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="e1b8a-106">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="e1b8a-107">Legt DDE-Freigabe Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-107">Sets DDE share information.</span></span> <span data-ttu-id="e1b8a-108">Dies erfolgt in der Regel nach der Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b8a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1b8a-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="e1b8a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1b8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b8a-111">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8a-112">Der Name des Servers, dessen DSDM geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="e1b8a-113">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8a-114">Der Name des Freigabe namens, dessen Informationen geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="e1b8a-115">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1b8a-116">*Nlevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8a-117">Die Informationsebene.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-117">The information level.</span></span> <span data-ttu-id="e1b8a-118">Dieser Parameter muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="e1b8a-119">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8a-120">Ein Zeiger auf die [**nddeshareinfo**](nddeshareinfo-str.md) -Struktur, die die DDE-Freigabe Informationen angibt, die in der DSDM gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="e1b8a-121">Derzeit werden die DDE-Freigabe Informationen als Ganzes geändert, d. h., es werden keine partiellen Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="e1b8a-122">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e1b8a-123">*cbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8a-124">Die Größe des *lpBuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e1b8a-125">*sparmnum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b8a-126">Der Parameter Index, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-126">The parameter index to be modified.</span></span> <span data-ttu-id="e1b8a-127">Die aktuelle Implementierung unterstützt keine partielle Änderung. Daher muss dieser Parameter NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b8a-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1b8a-128">Return value</span></span>

<span data-ttu-id="e1b8a-129">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="e1b8a-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="e1b8a-130">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1b8a-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b8a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1b8a-131">Requirements</span></span>



| <span data-ttu-id="e1b8a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1b8a-132">Requirement</span></span> | <span data-ttu-id="e1b8a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e1b8a-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b8a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1b8a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b8a-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1b8a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1b8a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b8a-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1b8a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e1b8a-138">Header</span><span class="sxs-lookup"><span data-stu-id="e1b8a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b8a-139"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b8a-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1b8a-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e1b8a-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1b8a-141"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1b8a-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e1b8a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e1b8a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b8a-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b8a-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1b8a-144">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e1b8a-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e1b8a-145">**Ndde sharesetinfow** (Unicode) und **nddebug** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e1b8a-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e1b8a-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1b8a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b8a-147">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="e1b8a-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="e1b8a-148">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e1b8a-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="e1b8a-149">**Nddebug-Info**</span><span class="sxs-lookup"><span data-stu-id="e1b8a-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="e1b8a-150">**Ndde sharegetinfo**</span><span class="sxs-lookup"><span data-stu-id="e1b8a-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




