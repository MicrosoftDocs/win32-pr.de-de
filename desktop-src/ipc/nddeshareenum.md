---
description: Ruft die Liste der verfügbaren DDE-Freigaben ab.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Ndde ShareEnum-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359196"
---
# <a name="nddeshareenum-function"></a><span data-ttu-id="9e883-103">Ndde ShareEnum-Funktion</span><span class="sxs-lookup"><span data-stu-id="9e883-103">NDdeShareEnum function</span></span>

<span data-ttu-id="9e883-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e883-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="9e883-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="9e883-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="9e883-106">Ruft die Liste der verfügbaren DDE-Freigaben ab.</span><span class="sxs-lookup"><span data-stu-id="9e883-106">Retrieves the list of available DDE shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e883-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e883-107">Syntax</span></span>


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="9e883-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e883-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e883-109">*lpszserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e883-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e883-110">Der Name des Servers, auf dem sich die DSDM befindet.</span><span class="sxs-lookup"><span data-stu-id="9e883-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="9e883-111">*Nlevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e883-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e883-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="9e883-112">Reserved.</span></span> <span data-ttu-id="9e883-113">Dieser Parameter muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9e883-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e883-114">*lpBuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9e883-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e883-115">Ein Zeiger auf einen Puffer, der die Liste der DDE-Freigaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="9e883-115">A pointer to a buffer that receives the list of DDE shares.</span></span> <span data-ttu-id="9e883-116">Die Liste der DDE-Freigaben wird als Sequenz von durch Null getrennten Zeichen folgen gespeichert, die mit einem doppelten NULL-Zeichen am Ende beendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e883-116">The list of DDE shares is stored as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="9e883-117">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="9e883-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="9e883-118">Wenn *lpBuffer* **null** ist, gibt die DSDM die Größe des Puffers zurück, der zum Speichern der Liste der Freigaben im *lpcbtotalavailable* -Parameter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9e883-118">If *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9e883-119">*cbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e883-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e883-120">Die Größe des *lpBuffer* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9e883-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="9e883-121">Dieser Parameter muss NULL sein, wenn *lpBuffer* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="9e883-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9e883-122">*lpnentriesread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9e883-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e883-123">Ein Zeiger auf eine Variable, die die Gesamtzahl der aufgelisteten Freigaben empfängt.</span><span class="sxs-lookup"><span data-stu-id="9e883-123">A pointer to a variable that receives the total number of shares being enumerated.</span></span> <span data-ttu-id="9e883-124">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9e883-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9e883-125">*lpcbtotalavailable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9e883-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e883-126">Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die im Puffer zum Speichern der Liste der DDE-Freigaben benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e883-126">A pointer to a variable that receives the total number of bytes needed in the buffer to store the list of DDE shares.</span></span> <span data-ttu-id="9e883-127">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9e883-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e883-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e883-128">Return value</span></span>

<span data-ttu-id="9e883-129">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".</span><span class="sxs-lookup"><span data-stu-id="9e883-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="9e883-130">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e883-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="9e883-131">Wenn der *lpBuffer* -Parameter **null** ist, wird ndde \_ buf \_ zu \_ klein zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e883-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e883-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e883-132">Requirements</span></span>



| <span data-ttu-id="9e883-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e883-133">Requirement</span></span> | <span data-ttu-id="9e883-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9e883-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e883-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e883-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9e883-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e883-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9e883-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e883-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9e883-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e883-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e883-139">Header</span><span class="sxs-lookup"><span data-stu-id="9e883-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e883-140"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e883-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e883-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e883-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e883-142"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e883-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e883-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9e883-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e883-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e883-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e883-145">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9e883-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9e883-146">**Ndde shareenumw** (Unicode) und **nddebug** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9e883-146">**NDdeShareEnumW** (Unicode) and **NDdeShareEnumA** (ANSI)</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="9e883-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e883-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e883-148">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="9e883-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="9e883-149">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9e883-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




