---
description: Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Ischaralpha anumschlag wrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978121"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="ea722-103">Ischaralpha anumschlag wrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="ea722-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="ea722-104">\[**Ischaralpha anumschlag wrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea722-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="ea722-105">Sie wird in nachfolgenden Versionen nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ea722-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="ea722-106">Sie sollten [**ischaralpha annumericw**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) anstelle von verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="ea722-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="ea722-107">Bestimmt, ob ein Zeichen entweder ein alphabetisches oder ein numerisches Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="ea722-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="ea722-108">Diese Bestimmung basiert auf der Semantik der Sprache, die während des Setups oder über die Systemsteuerung vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ea722-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="ea722-109">**Ischaralpha anumericwrapw** ist ein Wrapper für die **ischaralpha anumericw** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ea722-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="ea722-110">Weitere Hinweise zur Verwendung finden Sie auf der [**ischaralpha numerischen**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) Seite.</span><span class="sxs-lookup"><span data-stu-id="ea722-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ea722-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea722-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="ea722-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea722-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea722-113">*ch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea722-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea722-114">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="ea722-114">Type: **WCHAR**</span></span>

<span data-ttu-id="ea722-115">Das zu testende Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ea722-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea722-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea722-116">Return value</span></span>

<span data-ttu-id="ea722-117">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="ea722-117">Type: **BOOL**</span></span>

<span data-ttu-id="ea722-118">Wenn das Zeichen alphanumerisch ist, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ea722-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="ea722-119">Wenn das Zeichen nicht alphanumerisch ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ea722-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="ea722-120">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="ea722-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea722-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea722-121">Remarks</span></span>

<span data-ttu-id="ea722-122">**Ischaralpha anenumericwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen als Windows XP zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea722-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="ea722-123">Die bevorzugte Methode ist die Verwendung von [**ischaralpha annumericw**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="ea722-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="ea722-124">**Ischaralpha anumschlag wrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe von Ordnungszahl 28.</span><span class="sxs-lookup"><span data-stu-id="ea722-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea722-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ea722-125">Requirements</span></span>



| <span data-ttu-id="ea722-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea722-126">Requirement</span></span> | <span data-ttu-id="ea722-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ea722-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea722-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea722-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ea722-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea722-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea722-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea722-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ea722-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea722-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ea722-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ea722-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea722-133"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ea722-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea722-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ea722-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea722-135">**Ischaralpha numerisch**</span><span class="sxs-lookup"><span data-stu-id="ea722-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
