---
description: Ruft die Sicherheits Beschreibung ab, die der DDE-Freigabe zugeordnet ist. Dies erfolgt in der Regel zur Bearbeitung.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Nddebug-sharesecurity-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868352"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="02ce8-104">Ndde GetShareSecurity-Funktion</span><span class="sxs-lookup"><span data-stu-id="02ce8-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="02ce8-105">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="02ce8-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="02ce8-106">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="02ce8-107">Ruft die Sicherheits Beschreibung ab, die der DDE-Freigabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02ce8-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="02ce8-108">Dies erfolgt in der Regel zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="02ce8-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ce8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="02ce8-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="02ce8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="02ce8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ce8-111">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ce8-112">Der Name des Servers, auf dem sich die DSDM befindet.</span><span class="sxs-lookup"><span data-stu-id="02ce8-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="02ce8-113">*lpszsharename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ce8-114">Der Name der Freigabe, deren Sicherheits Beschreibung von der DSDM abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="02ce8-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="02ce8-115">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="02ce8-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="02ce8-116">*Si* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ce8-117">Ein [**Sicherheits \_ Informations**](/windows/desktop/SecAuthZ/security-information) Wert, der die Sicherheitsinformationen angibt, die aus der Sicherheits Beschreibung abgerufen werden sollen, die der Freigabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02ce8-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="02ce8-118">*pSD* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02ce8-119">Ein Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , die die selbst relative Sicherheits Beschreibung empfängt.</span><span class="sxs-lookup"><span data-stu-id="02ce8-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="02ce8-120">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="02ce8-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="02ce8-121">Wenn dieser Parameter **null** ist, bestimmt die DSDM die Größe der angeforderten Sicherheitsinformationen und gibt die Anzahl der Bytes zurück, die im *lpcbsdrequired* -Parameter benötigt werden, sowie den \_ zu kleinen ndde buf- \_ \_ Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="02ce8-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="02ce8-122">*cbsd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02ce8-123">Die Größe des *pSD* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="02ce8-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="02ce8-124">Dieser Parameter muss NULL sein, wenn das *pSD* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="02ce8-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="02ce8-125">*lpcbsdrequired* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02ce8-126">Ein Zeiger auf die Variable, die die tatsächliche Größe der abgerufenen Sicherheits Beschreibung empfängt.</span><span class="sxs-lookup"><span data-stu-id="02ce8-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="02ce8-127">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="02ce8-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ce8-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02ce8-128">Return value</span></span>

<span data-ttu-id="02ce8-129">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="02ce8-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="02ce8-130">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="02ce8-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="02ce8-131">Wenn der *pSD* -Parameter **null** war, wird ndde \_ buf \_ zu \_ klein zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="02ce8-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ce8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02ce8-132">Requirements</span></span>



| <span data-ttu-id="02ce8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02ce8-133">Requirement</span></span> | <span data-ttu-id="02ce8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="02ce8-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02ce8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02ce8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="02ce8-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="02ce8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02ce8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="02ce8-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02ce8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="02ce8-139">Header</span><span class="sxs-lookup"><span data-stu-id="02ce8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="02ce8-140"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ce8-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="02ce8-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02ce8-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="02ce8-142"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02ce8-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="02ce8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="02ce8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02ce8-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02ce8-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="02ce8-145">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="02ce8-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="02ce8-146">**Nddebug-sharesecurityw** (Unicode) und **nddebug** -Freigabe (ANSI)</span><span class="sxs-lookup"><span data-stu-id="02ce8-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="02ce8-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02ce8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ce8-148">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="02ce8-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="02ce8-149">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="02ce8-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="02ce8-150">**Sicherheits \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="02ce8-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="02ce8-151">**Ndde setsharesecurity**</span><span class="sxs-lookup"><span data-stu-id="02ce8-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

