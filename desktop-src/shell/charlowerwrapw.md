---
description: Konvertiert eine Unicode-Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Charlowerwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525400"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="60a62-103">Charlowerwrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="60a62-103">CharLowerWrapW function</span></span>

<span data-ttu-id="60a62-104">\[**Charlowerwrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60a62-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="60a62-105">Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60a62-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="60a62-106">Sie sollten " [**charlowerw**](/windows/win32/api/winuser/nf-winuser-charlowera) " an seiner Stelle verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="60a62-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="60a62-107">Konvertiert eine Unicode-Zeichenfolge oder ein einzelnes Zeichen in Kleinbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="60a62-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="60a62-108">Wenn der Operand eine Zeichenfolge ist, konvertiert die-Funktion die Zeichen an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="60a62-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="60a62-109">**Charlowerwrapw** ist ein Wrapper für die Funktion " **charlowerw** ".</span><span class="sxs-lookup"><span data-stu-id="60a62-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="60a62-110">Weitere Hinweise zur Verwendung finden Sie auf der Seite [**charlower**](/windows/win32/api/winuser/nf-winuser-charlowera) .</span><span class="sxs-lookup"><span data-stu-id="60a62-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="60a62-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="60a62-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="60a62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="60a62-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60a62-113">*PCH* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="60a62-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60a62-114">Typ: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="60a62-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="60a62-115">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge oder ein einzelnes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60a62-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="60a62-116">Wenn das höchst wertige Wort dieses Parameters NULL ist, muss das nieder wertige Wort nur ein einzelnes Zeichen enthalten, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60a62-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60a62-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60a62-117">Return value</span></span>

<span data-ttu-id="60a62-118">Typ: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="60a62-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="60a62-119">Wenn *PCH* eine Zeichenfolge ist, gibt die Funktion einen Zeiger auf die konvertierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="60a62-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="60a62-120">Da die Zeichenfolge direkt konvertiert wird, entspricht der Rückgabewert dem *PCH*.</span><span class="sxs-lookup"><span data-stu-id="60a62-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="60a62-121">Wenn *PCH* ein einzelnes Zeichen ist, ist der Rückgabewert ein 32-Bit-Wert, dessen hohes Wort 0 (null) ist, und das nieder wertige Wort enthält das konvertierte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="60a62-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="60a62-122">Es gibt keinen Hinweis auf Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="60a62-122">There is no indication of success or failure.</span></span> <span data-ttu-id="60a62-123">Der Fehler tritt selten auf.</span><span class="sxs-lookup"><span data-stu-id="60a62-123">Failure is rare.</span></span> <span data-ttu-id="60a62-124">Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="60a62-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="60a62-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60a62-125">Remarks</span></span>

<span data-ttu-id="60a62-126">Die bevorzugte Methode ist die Verwendung von [**charlowerw**](/windows/win32/api/winuser/nf-winuser-charlowera) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="60a62-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="60a62-127">**Charlowerwrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 38 verwendet.</span><span class="sxs-lookup"><span data-stu-id="60a62-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="60a62-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="60a62-128">Requirements</span></span>



| <span data-ttu-id="60a62-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60a62-129">Requirement</span></span> | <span data-ttu-id="60a62-130">Wert</span><span class="sxs-lookup"><span data-stu-id="60a62-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60a62-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60a62-131">Minimum supported client</span></span><br/> | <span data-ttu-id="60a62-132">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60a62-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60a62-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60a62-133">Minimum supported server</span></span><br/> | <span data-ttu-id="60a62-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60a62-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="60a62-135">DLL</span><span class="sxs-lookup"><span data-stu-id="60a62-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60a62-136"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="60a62-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60a62-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60a62-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a62-138">**Charlower**</span><span class="sxs-lookup"><span data-stu-id="60a62-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
