---
description: Zeigt ein Dialogfeld an, in dem die Signatur Geber Informationen für eine signierte Nachricht enthalten sind.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: CryptUIDlgViewSignerInfo-Funktion
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862311"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="7a89c-103">CryptUIDlgViewSignerInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a89c-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="7a89c-104">\[Die **cryptuidlgviewsignerinfo** -Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7a89c-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7a89c-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7a89c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7a89c-106">\]</span><span class="sxs-lookup"><span data-stu-id="7a89c-106">\]</span></span>

<span data-ttu-id="7a89c-107">Die Funktion **cryptuidlgviewsignerinfo** zeigt ein Dialogfeld an, in dem die Signatur Geber Informationen für eine signierte Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7a89c-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="7a89c-108">Diese Funktion ist nicht in einer veröffentlichten Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="7a89c-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="7a89c-109">Um diese Struktur zu verwenden, deklarieren Sie Sie im exakten Format.</span><span class="sxs-lookup"><span data-stu-id="7a89c-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a89c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a89c-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="7a89c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a89c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a89c-112">*pcvsi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a89c-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a89c-113">Ein Zeiger auf eine [**cryptui \_ viewsignerinfo \_**](cryptui-viewsignerinfo-struct.md) -Struktur Struktur, die die anzuzeigenden Signatur Geber Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7a89c-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a89c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a89c-114">Return value</span></span>

<span data-ttu-id="7a89c-115">Diese Funktion gibt bei Erfolg einen Wert ungleich 0 (null) und NULL bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7a89c-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="7a89c-116">Für erweiterte Fehlerinformationen aufrufen Sie die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7a89c-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="7a89c-117">Mögliche Fehlercodes von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="7a89c-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7a89c-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7a89c-118">Return code</span></span>                                                                                   | <span data-ttu-id="7a89c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a89c-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7a89c-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7a89c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7a89c-121">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7a89c-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="7a89c-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7a89c-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7a89c-123">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7a89c-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="7a89c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a89c-124">Requirements</span></span>



| <span data-ttu-id="7a89c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a89c-125">Requirement</span></span> | <span data-ttu-id="7a89c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7a89c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a89c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a89c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7a89c-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a89c-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a89c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a89c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7a89c-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a89c-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a89c-131">Ende des Supports</span><span class="sxs-lookup"><span data-stu-id="7a89c-131">End of support</span></span><br/> | <span data-ttu-id="7a89c-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a89c-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7a89c-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a89c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a89c-134"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a89c-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="7a89c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7a89c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a89c-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a89c-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="7a89c-137">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="7a89c-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a89c-138">**Cryptuidlgviewsignerinfow** (Unicode) und **cryptuidlgviewsignerinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7a89c-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a89c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a89c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a89c-140">**cryptui \_ viewsignerinfo- \_ Struktur**</span><span class="sxs-lookup"><span data-stu-id="7a89c-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
