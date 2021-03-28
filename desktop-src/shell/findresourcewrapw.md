---
description: Bestimmt den Speicherort einer Ressource mit dem angegebenen Typ und Namen im angegebenen Modul.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Findresourcewrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215958"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="289f7-103">Findresourcewrapw-Funktion</span><span class="sxs-lookup"><span data-stu-id="289f7-103">FindResourceWrapW function</span></span>

<span data-ttu-id="289f7-104">\[**Findresourcewrapw** ist für die Verwendung in Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="289f7-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="289f7-105">Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="289f7-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="289f7-106">Sie sollten stattdessen [**findresourcew**](/windows/win32/api/winbase/nf-winbase-findresourcea) verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="289f7-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="289f7-107">Bestimmt den Speicherort einer Ressource mit dem angegebenen Typ und Namen im angegebenen Modul.</span><span class="sxs-lookup"><span data-stu-id="289f7-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="289f7-108">**Findresourcewrapw** ist ein Wrapper für die **findresourcew** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="289f7-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="289f7-109">Weitere Hinweise zur Verwendung finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .</span><span class="sxs-lookup"><span data-stu-id="289f7-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="289f7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="289f7-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="289f7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="289f7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="289f7-112">*HMODULE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="289f7-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289f7-113">Typ: **HMODULE**</span><span class="sxs-lookup"><span data-stu-id="289f7-113">Type: **HMODULE**</span></span>

<span data-ttu-id="289f7-114">Ein Handle für das Modul, dessen ausführbare Datei die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="289f7-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="289f7-115">Der Wert **null** gibt das Modul Handle an, das der Bilddatei zugeordnet ist, die vom Betriebssystem zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="289f7-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="289f7-116">*lpname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="289f7-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289f7-117">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="289f7-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="289f7-118">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="289f7-118">The name of the resource.</span></span> <span data-ttu-id="289f7-119">Weitere Informationen finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="289f7-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="289f7-120">*lptype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="289f7-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="289f7-121">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="289f7-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="289f7-122">Ein Zeiger auf eine Zeichenfolge, die den Ressourcentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="289f7-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="289f7-123">Weitere Informationen finden Sie unter [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="289f7-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="289f7-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="289f7-124">Return value</span></span>

<span data-ttu-id="289f7-125">Typ: **hrsrc**</span><span class="sxs-lookup"><span data-stu-id="289f7-125">Type: **HRSRC**</span></span>

<span data-ttu-id="289f7-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für den Informationsblock der angegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="289f7-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="289f7-127">Um ein Handle für die Ressource zu erhalten, übergeben Sie dieses Handle an die [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="289f7-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="289f7-128">Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="289f7-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="289f7-129">Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="289f7-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="289f7-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="289f7-130">Remarks</span></span>

<span data-ttu-id="289f7-131">Wenn Sie eine bestimmte Lokalisierung angeben müssen, verwenden Sie die Funktion [**findresourceex**](/windows/win32/api/winbase/nf-winbase-findresourceexa) anstelle von **findresourcewrapw**.</span><span class="sxs-lookup"><span data-stu-id="289f7-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="289f7-132">**Findresourcewrapw** bietet die Möglichkeit, Unicode-Zeichen folgen in älteren Betriebssystemen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="289f7-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="289f7-133">Die bevorzugte Methode ist die Verwendung von [**findresourcew**](/windows/win32/api/winbase/nf-winbase-findresourcea) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="289f7-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="289f7-134">**Findresourcewrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 66 verwendet.</span><span class="sxs-lookup"><span data-stu-id="289f7-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="289f7-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="289f7-135">Requirements</span></span>



| <span data-ttu-id="289f7-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="289f7-136">Requirement</span></span> | <span data-ttu-id="289f7-137">Wert</span><span class="sxs-lookup"><span data-stu-id="289f7-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="289f7-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="289f7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="289f7-139">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="289f7-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="289f7-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="289f7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="289f7-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="289f7-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="289f7-142">Header</span><span class="sxs-lookup"><span data-stu-id="289f7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="289f7-143"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="289f7-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="289f7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="289f7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="289f7-145"><dt>Shlwapi.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="289f7-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="289f7-146">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="289f7-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="289f7-147">**Findresourcewrapw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="289f7-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="289f7-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="289f7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289f7-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="289f7-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
