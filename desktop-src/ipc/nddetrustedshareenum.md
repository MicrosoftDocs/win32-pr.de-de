---
description: Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Nddebug-ShareEnum-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348248"
---
# <a name="nddetrustedshareenum-function"></a><span data-ttu-id="0de79-103">Nddebug-ShareEnum-Funktion</span><span class="sxs-lookup"><span data-stu-id="0de79-103">NDdeTrustedShareEnum function</span></span>

<span data-ttu-id="0de79-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0de79-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="0de79-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="0de79-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="0de79-106">Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="0de79-106">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de79-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0de79-107">Syntax</span></span>


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="0de79-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0de79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de79-109">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0de79-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de79-110">Der Name des Servers, auf dem sich die DSDM befindet.</span><span class="sxs-lookup"><span data-stu-id="0de79-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-111">*Nlevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0de79-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de79-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="0de79-112">Reserved.</span></span> <span data-ttu-id="0de79-113">Dieser Parameter muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0de79-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-114">*lpBuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0de79-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0de79-115">Ein Zeiger auf einen Puffer, der die Liste der vertrauenswürdigen DDE-Freigaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="0de79-115">A pointer to a buffer that receives the list of trusted DDE shares.</span></span> <span data-ttu-id="0de79-116">Die Liste der vertrauenswürdigen DDE-Freigaben wird als Sequenz von durch Null getrennten Zeichen folgen zurückgegeben, die mit einem doppelten NULL-Zeichen am Ende beendet werden.</span><span class="sxs-lookup"><span data-stu-id="0de79-116">The list of trusted DDE shares is returned as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="0de79-117">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="0de79-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="0de79-118">Wenn der *lpBuffer* **null** ist, gibt die DSDM die Größe des Puffers zurück, der zum Speichern der Liste der Freigaben im Feld *lpcbtotalavailable* erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0de79-118">If the *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* field.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-119">*cbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0de79-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de79-120">Die Größe des *lpBuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0de79-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="0de79-121">Dieser Parameter muss NULL sein, wenn *lpBuffer* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="0de79-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-122">*lpnentriesread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0de79-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0de79-123">Ein Zeiger auf eine Variable, die die Gesamtzahl der aufzuzählenden vertrauenswürdigen Freigaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="0de79-123">A pointer to a variable that receives the total number of trusted shares being enumerated.</span></span> <span data-ttu-id="0de79-124">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0de79-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-125">*lpcbtotalavailable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0de79-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0de79-126">Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die zum Speichern der Liste vertrauenswürdiger DDE-Freigaben benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="0de79-126">A pointer to a variable that receives the total number of bytes needed to store the list of trusted DDE shares.</span></span> <span data-ttu-id="0de79-127">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0de79-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de79-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0de79-128">Return value</span></span>

<span data-ttu-id="0de79-129">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="0de79-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="0de79-130">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0de79-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="0de79-131">Wenn der *lpBuffer* -Parameter **null** ist, wird ndde \_ buf \_ zu \_ klein zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0de79-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de79-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0de79-132">Requirements</span></span>



| <span data-ttu-id="0de79-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0de79-133">Requirement</span></span> | <span data-ttu-id="0de79-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0de79-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0de79-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0de79-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0de79-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0de79-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0de79-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0de79-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0de79-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0de79-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0de79-139">Header</span><span class="sxs-lookup"><span data-stu-id="0de79-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0de79-140"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="0de79-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0de79-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0de79-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="0de79-142"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0de79-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0de79-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0de79-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0de79-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0de79-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="0de79-145">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="0de79-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0de79-146">**Nddebug-shareenumw** (Unicode) und **nddebug-shareenuma** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0de79-146">**NDdeTrustedShareEnumW** (Unicode) and **NDdeTrustedShareEnumA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="0de79-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0de79-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de79-148">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="0de79-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="0de79-149">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0de79-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




