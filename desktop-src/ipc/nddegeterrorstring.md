---
description: Konvertiert einen Fehlercode, der von einer Network DDE-Funktion zurückgegeben wird, in eine Fehler Zeichenfolge, die den zurückgegebenen Fehlercode
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Nddebug. String-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041591"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="fc682-103">Nddebug-terrorstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="fc682-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="fc682-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fc682-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="fc682-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="fc682-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="fc682-106">Konvertiert einen Fehlercode, der von einer Network DDE-Funktion zurückgegeben wird, in eine Fehler Zeichenfolge, die den zurückgegebenen Fehlercode</span><span class="sxs-lookup"><span data-stu-id="fc682-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc682-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc682-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="fc682-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc682-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc682-109">*uerrorcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc682-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc682-110">Der Fehlercode, der in eine Fehler Zeichenfolge konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc682-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="fc682-111">*lpszerrorstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fc682-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc682-112">Ein Zeiger auf einen Puffer, der die übersetzte Fehler Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="fc682-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="fc682-113">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="fc682-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="fc682-114">Wenn der Puffer nicht groß genug ist, um die gesamte Fehler Zeichenfolge zu speichern, wird die Zeichenfolge abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="fc682-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="fc682-115">*cbubsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc682-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc682-116">Die Größe des Puffers, der die Fehler Zeichenfolge empfängt, in **tchars**.</span><span class="sxs-lookup"><span data-stu-id="fc682-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc682-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc682-117">Return value</span></span>

<span data-ttu-id="fc682-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert „0“.</span><span class="sxs-lookup"><span data-stu-id="fc682-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="fc682-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fc682-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="fc682-120">Wenn der *lpszerrorstring* -Puffer nicht groß genug ist, um die gesamte Fehler Zeichenfolge zu akzeptieren, und die Zeichenfolge abgeschnitten wird, gibt die Funktion den Wert "ndde \_ internal error" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="fc682-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc682-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc682-121">Requirements</span></span>



| <span data-ttu-id="fc682-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc682-122">Requirement</span></span> | <span data-ttu-id="fc682-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fc682-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc682-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc682-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fc682-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc682-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fc682-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc682-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fc682-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc682-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc682-128">Header</span><span class="sxs-lookup"><span data-stu-id="fc682-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc682-129"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc682-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc682-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fc682-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc682-131"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc682-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc682-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fc682-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc682-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc682-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc682-134">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="fc682-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fc682-135">**Ndbegeterrorstringw** (Unicode) und **nddebug** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fc682-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="fc682-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc682-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc682-137">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="fc682-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="fc682-138">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fc682-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




