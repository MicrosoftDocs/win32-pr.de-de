---
description: Liest eine Zeile aus der Datei "Setup. inf" und extrahiert das angegebene Feld aus der Zeichenfolge.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Parametefield-Funktion (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216607"
---
# <a name="parsefield-function"></a><span data-ttu-id="fd102-103">Parametefield-Funktion</span><span class="sxs-lookup"><span data-stu-id="fd102-103">ParseField function</span></span>

<span data-ttu-id="fd102-104">\[In der nächsten Version des Microsoft Windows-Betriebssystems ist es derzeit wahrscheinlich, dass die Funktion " **Parser Field** " für die Verwendung in der nächsten Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fd102-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="fd102-105">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fd102-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="fd102-106">Liest eine Zeile aus der Datei "Setup. inf" und extrahiert das angegebene Feld aus der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fd102-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd102-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd102-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="fd102-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd102-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd102-109">*szdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd102-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd102-110">Geben Sie Folgendes ein: \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="fd102-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="fd102-111">Ein Zeiger auf die Zeile aus der Datei "Setup. inf".</span><span class="sxs-lookup"><span data-stu-id="fd102-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="fd102-112">_N \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd102-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd102-113">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="fd102-113">Type: **int**</span></span>

<span data-ttu-id="fd102-114">**Int** , der angibt, welches Feld extrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd102-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="fd102-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="fd102-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="fd102-116">Gibt das Feld vor einem Gleichheitszeichen (=) an.</span><span class="sxs-lookup"><span data-stu-id="fd102-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="fd102-117">(1)</span><span class="sxs-lookup"><span data-stu-id="fd102-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="fd102-118">Gibt das erste Feld an.</span><span class="sxs-lookup"><span data-stu-id="fd102-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fd102-119">*szbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd102-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd102-120">Typ: \**LPTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="fd102-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="fd102-121">Ein Zeiger auf den Puffer, der das extrahierte Feld empfängt.</span><span class="sxs-lookup"><span data-stu-id="fd102-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="fd102-122">_iBufLen \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd102-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd102-123">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="fd102-123">Type: **int**</span></span>

<span data-ttu-id="fd102-124">**Int** , der die Größe des Puffers empfängt, der das extrahierte Feld empfängt.</span><span class="sxs-lookup"><span data-stu-id="fd102-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd102-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd102-125">Return value</span></span>

<span data-ttu-id="fd102-126">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="fd102-126">Type: **bool**</span></span>

<span data-ttu-id="fd102-127">Gibt **true** zurück, wenn die Funktion erfolgreich ist, und **false** , wenn Sie fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="fd102-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd102-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd102-128">Remarks</span></span>

<span data-ttu-id="fd102-129">Die Felder in der Zeichenfolge müssen durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="fd102-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="fd102-130">Führende und nachfolgende Leerzeichen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="fd102-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd102-131">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fd102-131">Requirements</span></span>



| <span data-ttu-id="fd102-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd102-132">Requirement</span></span> | <span data-ttu-id="fd102-133">Wert</span><span class="sxs-lookup"><span data-stu-id="fd102-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd102-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd102-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fd102-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd102-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd102-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd102-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fd102-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd102-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd102-138">Header</span><span class="sxs-lookup"><span data-stu-id="fd102-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd102-139"><dt>Util. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd102-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="fd102-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd102-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd102-141"><dt>Shell32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd102-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="fd102-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fd102-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd102-143"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fd102-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




