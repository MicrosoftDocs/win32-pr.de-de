---
description: Sendet eine Unicode-Zeichenfolge zur Anzeige an den Debugger.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Outputdebug-Funktion (shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994822"
---
# <a name="outputdebugstringwrapw-function"></a><span data-ttu-id="b11c6-103">Outputdebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="b11c6-103">OutputDebugStringWrapW function</span></span>

<span data-ttu-id="b11c6-104">\[Diese Funktion ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b11c6-104">\[This function is available for use in Windows XP.</span></span> <span data-ttu-id="b11c6-105">Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b11c6-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="b11c6-106">Verwenden Sie [**outputentbugstringw**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) an seiner Stelle.\]</span><span class="sxs-lookup"><span data-stu-id="b11c6-106">Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in its place.\]</span></span>

<span data-ttu-id="b11c6-107">Sendet eine Unicode-Zeichenfolge zur Anzeige an den Debugger.</span><span class="sxs-lookup"><span data-stu-id="b11c6-107">Sends a Unicode string to the debugger for display.</span></span>

> [!Note]  
> <span data-ttu-id="b11c6-108">**Outputentbugstringwrapw** ist ein Wrapper für die **outputdebug** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b11c6-108">**OutputDebugStringWrapW** is a wrapper for the **OutputDebugStringW** function.</span></span> <span data-ttu-id="b11c6-109">Weitere Hinweise zur Verwendung finden Sie auf der Seite [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .</span><span class="sxs-lookup"><span data-stu-id="b11c6-109">See the [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b11c6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b11c6-110">Syntax</span></span>


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a><span data-ttu-id="b11c6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b11c6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b11c6-112">*lpoutputstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b11c6-112">*lpOutputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b11c6-113">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b11c6-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b11c6-114">Ein Zeiger auf die auf NULL endende Unicode-Zeichenfolge, die angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b11c6-114">A pointer to the null-terminated Unicode string to be displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b11c6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b11c6-115">Return value</span></span>

<span data-ttu-id="b11c6-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b11c6-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b11c6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b11c6-117">Remarks</span></span>

<span data-ttu-id="b11c6-118">**Outputdebugstringwrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in Betriebssystemen vor Windows XP zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b11c6-118">**OutputDebugStringWrapW** provides the ability to use Unicode strings in operating systems prior to Windows XP.</span></span> <span data-ttu-id="b11c6-119">Die bevorzugte Methode ist die Verwendung von [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="b11c6-119">The preferred method is to use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="b11c6-120">**Outputdebug-wrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 115 verwendet.</span><span class="sxs-lookup"><span data-stu-id="b11c6-120">**OutputDebugStringWrapW** must be called directly from Shlwapi.dll, using ordinal 115.</span></span>

<span data-ttu-id="b11c6-121">Wenn die Anwendung über keinen Debugger verfügt, zeigt der System Debugger die Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="b11c6-121">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="b11c6-122">Wenn die Anwendung keinen Debugger hat und der System Debugger nicht aktiv ist, führt **outputdebugstringwrapw keine Aktion** aus.</span><span class="sxs-lookup"><span data-stu-id="b11c6-122">If the application has no debugger and the system debugger is not active, **OutputDebugStringWrapW** does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b11c6-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b11c6-123">Requirements</span></span>



| <span data-ttu-id="b11c6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b11c6-124">Requirement</span></span> | <span data-ttu-id="b11c6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b11c6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b11c6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b11c6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b11c6-127">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b11c6-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b11c6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b11c6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b11c6-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b11c6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b11c6-130">Header</span><span class="sxs-lookup"><span data-stu-id="b11c6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b11c6-131"><dt>Shlwapip. h</dt></span><span class="sxs-lookup"><span data-stu-id="b11c6-131"><dt>Shlwapip.h</dt></span></span> </dl>                         |
| <span data-ttu-id="b11c6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b11c6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b11c6-133"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b11c6-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b11c6-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b11c6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b11c6-135">**OutputDebugString**</span><span class="sxs-lookup"><span data-stu-id="b11c6-135">**OutputDebugString**</span></span>](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
