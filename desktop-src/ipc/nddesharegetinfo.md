---
description: Ruft DDE-Freigabe Informationen ab. Dies erfolgt in der Regel zur Bearbeitung.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Ndde sharegetinfo-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344649"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="fe98e-104">Nddebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe98e-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="fe98e-105">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fe98e-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="fe98e-106">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="fe98e-107">Ruft DDE-Freigabe Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="fe98e-107">Retrieves DDE share information.</span></span> <span data-ttu-id="fe98e-108">Dies erfolgt in der Regel zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="fe98e-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe98e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe98e-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="fe98e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe98e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe98e-111">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-112">Der Name des Servers, auf dem sich die DSDM befindet.</span><span class="sxs-lookup"><span data-stu-id="fe98e-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="fe98e-113">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-114">Der Freigabe Name, dessen Informationen aus dem DSDM abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fe98e-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="fe98e-115">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fe98e-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe98e-116">*Nlevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-117">Die Informationsebene.</span><span class="sxs-lookup"><span data-stu-id="fe98e-117">The information level.</span></span> <span data-ttu-id="fe98e-118">Dieser Parameter muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="fe98e-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="fe98e-119">*lpBuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-120">Ein Zeiger auf einen Puffer, der die [**ndbeshareingefo**](nddeshareinfo-str.md) -Struktur und die zugehörigen Daten empfängt, auf die von den Membern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fe98e-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="fe98e-121">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="fe98e-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="fe98e-122">Wenn *lpBuffer* **null** ist, berechnet die DSDM die Anzahl der Bytes, die zum Speichern der angeforderten Freigabe Informationen erforderlich sind, und gibt diesen Wert im Feld *lpntotalavailable* zusammen mit dem \_ zu kleinen ndde buf- \_ Fehler zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="fe98e-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="fe98e-123">*cbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-124">Die Größe des *lpBuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fe98e-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="fe98e-125">Wenn *lpBuffer* den Wert **null** hat, sollte *cbubsize* gleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="fe98e-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fe98e-126">*lpntotalavailable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-127">Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die zum Speichern der angeforderten Freigabe Informationen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="fe98e-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="fe98e-128">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fe98e-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe98e-129">*lpnitems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe98e-130">Ein Zeiger auf eine Elementauswahl Maske für das Abrufen partieller Freigabe Informationen.</span><span class="sxs-lookup"><span data-stu-id="fe98e-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe98e-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe98e-131">Return value</span></span>

<span data-ttu-id="fe98e-132">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="fe98e-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="fe98e-133">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe98e-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="fe98e-134">Wenn der *lpBuffer* -Parameter **null** ist, wird ndde \_ buf \_ zu \_ klein zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe98e-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe98e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe98e-135">Requirements</span></span>



| <span data-ttu-id="fe98e-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe98e-136">Requirement</span></span> | <span data-ttu-id="fe98e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="fe98e-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe98e-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe98e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fe98e-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe98e-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe98e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fe98e-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe98e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe98e-142">Header</span><span class="sxs-lookup"><span data-stu-id="fe98e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe98e-143"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe98e-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe98e-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe98e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe98e-145"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe98e-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe98e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fe98e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe98e-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe98e-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe98e-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fe98e-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe98e-149">**Nddebug** (Unicode) und **ndabsharegetinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fe98e-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fe98e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe98e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe98e-151">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="fe98e-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="fe98e-152">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe98e-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="fe98e-153">**Nddebug-Info**</span><span class="sxs-lookup"><span data-stu-id="fe98e-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="fe98e-154">**Nddesharesetinfo**</span><span class="sxs-lookup"><span data-stu-id="fe98e-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




