---
description: Konvertiert eine Zeichenfolge in eine GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864939"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="ba5ff-103">GUIDFromString-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba5ff-103">GUIDFromString function</span></span>

<span data-ttu-id="ba5ff-104">\[" **GUIDFromString** " ist über Windows XP mit Service Pack 2 (SP2) oder Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="ba5ff-105">Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ba5ff-106">Anwendungen sollten anstelle dieser Funktion " [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) " oder " [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) " verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="ba5ff-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="ba5ff-107">Konvertiert eine Zeichenfolge in eine GUID.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba5ff-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="ba5ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba5ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5ff-110">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba5ff-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5ff-111">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="ba5ff-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="ba5ff-112">Ein Zeiger auf die zu konvertierende NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="ba5ff-113">Die Zeichenfolge sollte in der folgenden Form vorliegen:</span><span class="sxs-lookup"><span data-stu-id="ba5ff-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="ba5ff-114">*pguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ba5ff-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5ff-115">Typ: **lpguid**</span><span class="sxs-lookup"><span data-stu-id="ba5ff-115">Type: **LPGUID**</span></span>

<span data-ttu-id="ba5ff-116">Zeiger auf einen Puffer, um die GUID zu erhalten, wenn diese Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5ff-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba5ff-117">Return value</span></span>

<span data-ttu-id="ba5ff-118">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="ba5ff-118">Type: **BOOL**</span></span>

<span data-ttu-id="ba5ff-119">**True** , wenn die GUID erfolgreich erstellt wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba5ff-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba5ff-120">Remarks</span></span>

<span data-ttu-id="ba5ff-121">Diese Funktion wird nicht in einem Header deklariert oder nach Name aus einer DLL-Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="ba5ff-122">Sie muss aus Shell32.dll als Ordnungszahl 703 für **guidfromstraninga** und Ordnungszahl 704 für **guidfromstringw** geladen werden.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="ba5ff-123">Sie können auch von Shlwapi.dll als Ordnungszahl 269 für **guidfromstraninga** und Ordnungszahl 270 für **guidfromstringw** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ba5ff-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5ff-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ba5ff-124">Requirements</span></span>



| <span data-ttu-id="ba5ff-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba5ff-125">Requirement</span></span> | <span data-ttu-id="ba5ff-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ba5ff-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5ff-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba5ff-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5ff-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba5ff-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ba5ff-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba5ff-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5ff-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba5ff-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ba5ff-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ba5ff-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba5ff-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba5ff-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="ba5ff-133">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ba5ff-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ba5ff-134">**Guidfromstringw** (Unicode) und **guidfromstraninga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ba5ff-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
