---
description: Konvertiert klein geschriebene Zeichen in einem Puffer in Großbuchstaben.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Charupperbuffwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525397"
---
# <a name="charupperbuffwrapw-function"></a><span data-ttu-id="20f62-103">Charupperbuffwrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="20f62-103">CharUpperBuffWrapW function</span></span>

<span data-ttu-id="20f62-104">\[**Charupperbuffwrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20f62-104">\[**CharUpperBuffWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="20f62-105">Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20f62-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="20f62-106">Sie sollten an seiner Stelle [**charupperbuffw**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="20f62-106">You should use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in its place.\]</span></span>

<span data-ttu-id="20f62-107">Konvertiert klein geschriebene Zeichen in einem Puffer in Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="20f62-107">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="20f62-108">Die-Funktion konvertiert die Zeichen an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="20f62-108">The function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="20f62-109">**Charupperbuffwrapw** ist ein Wrapper für die **charupperbuffw** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="20f62-109">**CharUpperBuffWrapW** is a wrapper for the **CharUpperBuffW** function.</span></span> <span data-ttu-id="20f62-110">Weitere Hinweise zur Verwendung finden Sie auf der Seite [**charupperbuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .</span><span class="sxs-lookup"><span data-stu-id="20f62-110">See the [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="20f62-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="20f62-111">Syntax</span></span>


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a><span data-ttu-id="20f62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="20f62-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f62-113">*PCH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20f62-113">*pch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20f62-114">Typ: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="20f62-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="20f62-115">Ein Zeiger auf einen Puffer, der ein oder mehrere zu verarbeitende Unicode-Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="20f62-115">A pointer to a buffer that contains one or more Unicode characters to process.</span></span>

</dd> <dt>

<span data-ttu-id="20f62-116">*cchlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20f62-116">*cchLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20f62-117">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="20f62-117">Type: **DWORD**</span></span>

<span data-ttu-id="20f62-118">Gibt die Größe des Puffers, auf den *PCH* zeigt, in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="20f62-118">Specifies the size, in characters, of the buffer pointed to by *pch*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f62-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20f62-119">Return value</span></span>

<span data-ttu-id="20f62-120">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="20f62-120">Type: **DWORD**</span></span>

<span data-ttu-id="20f62-121">Die Anzahl der verarbeiteten Zeichen.</span><span class="sxs-lookup"><span data-stu-id="20f62-121">The number of characters processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="20f62-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20f62-122">Remarks</span></span>

<span data-ttu-id="20f62-123">Die bevorzugte Methode ist die Verwendung von [**charupperbuffw**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="20f62-123">The preferred method is to use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="20f62-124">**Charupperbuffwrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe der Ordinalzahl 44.</span><span class="sxs-lookup"><span data-stu-id="20f62-124">**CharUpperBuffWrapW** must be called directly from Shlwapi.dll, using ordinal 44.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f62-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="20f62-125">Requirements</span></span>



| <span data-ttu-id="20f62-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20f62-126">Requirement</span></span> | <span data-ttu-id="20f62-127">Wert</span><span class="sxs-lookup"><span data-stu-id="20f62-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f62-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20f62-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20f62-129">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20f62-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20f62-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20f62-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20f62-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20f62-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="20f62-132">DLL</span><span class="sxs-lookup"><span data-stu-id="20f62-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20f62-133"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="20f62-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f62-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="20f62-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f62-135">**Charupperbuff**</span><span class="sxs-lookup"><span data-stu-id="20f62-135">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
