---
description: Hebt die Registrierung einer Fenster Klasse auf, die von linkwindow \_ registerClass registriert wird.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980017"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="bbddf-103">Linkwindow \_ unregisterclass-Funktion</span><span class="sxs-lookup"><span data-stu-id="bbddf-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="bbddf-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bbddf-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="bbddf-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bbddf-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bbddf-106">Hebt die Registrierung einer Fenster Klasse auf, die von [**linkwindow \_ registerClass**](linkwindow-registerclass.md)registriert wird.</span><span class="sxs-lookup"><span data-stu-id="bbddf-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbddf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbddf-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="bbddf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbddf-108">Parameters</span></span>

<span data-ttu-id="bbddf-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bbddf-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbddf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbddf-110">Return value</span></span>

<span data-ttu-id="bbddf-111">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="bbddf-111">Type: **BOOL**</span></span>

<span data-ttu-id="bbddf-112">Gibt **true** zurück, wenn der Vorgang erfolgreich war. Andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="bbddf-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbddf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbddf-113">Remarks</span></span>

<span data-ttu-id="bbddf-114">Diese Funktion verfügt über keine zugeordnete Header-oder Bibliotheksdatei, sodass Sie von Ordinalwerten aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="bbddf-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="bbddf-115">Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen Shell32.dll, um ein Modul Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bbddf-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="bbddf-116">Dann rufe Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und der Ordinalzahl 259 auf, um diese Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbddf-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbddf-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bbddf-117">Requirements</span></span>



| <span data-ttu-id="bbddf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbddf-118">Requirement</span></span> | <span data-ttu-id="bbddf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bbddf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbddf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbddf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbddf-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbddf-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbddf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbddf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbddf-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbddf-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bbddf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bbddf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbddf-125"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="bbddf-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbddf-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bbddf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbddf-127">Übersicht über Syslink-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="bbddf-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
