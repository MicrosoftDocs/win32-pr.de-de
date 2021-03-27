---
description: Registriert eine Fenster Klasse, mit der das allgemeine Syslink-Steuerelement in einem Fenster verwendet werden kann.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980024"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="9307b-103">Linkwindow- \_ registerClass-Funktion</span><span class="sxs-lookup"><span data-stu-id="9307b-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="9307b-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9307b-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="9307b-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9307b-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="9307b-106">Verwenden Sie stattdessen [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]</span><span class="sxs-lookup"><span data-stu-id="9307b-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="9307b-107">Registriert eine Fenster Klasse, mit der das allgemeine [Syslink](../controls/syslink-overview.md) -Steuerelement in einem Fenster verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9307b-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9307b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9307b-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="9307b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9307b-109">Parameters</span></span>

<span data-ttu-id="9307b-110">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9307b-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9307b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9307b-111">Return value</span></span>

<span data-ttu-id="9307b-112">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="9307b-112">Type: **BOOL**</span></span>

<span data-ttu-id="9307b-113">Gibt **true** zurück, wenn die Registrierung erfolgreich war. Andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9307b-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9307b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9307b-114">Remarks</span></span>

<span data-ttu-id="9307b-115">Diese Funktion verfügt über keine zugeordnete Header-oder Bibliotheksdatei, sodass Sie von Ordinalwerten aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="9307b-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="9307b-116">Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen Shell32.dll, um ein Modul Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9307b-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="9307b-117">Dann rufe Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und der Ordinalzahl 258 auf, um diese Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9307b-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="9307b-118">Verwenden Sie [**linkwindow \_ unregisterclass**](linkwindow-unregisterclass.md) , um die Registrierung der Klasse nach der Verwendung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="9307b-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="9307b-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9307b-119">Requirements</span></span>



| <span data-ttu-id="9307b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9307b-120">Requirement</span></span> | <span data-ttu-id="9307b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9307b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9307b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9307b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9307b-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9307b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9307b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9307b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9307b-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9307b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9307b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9307b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9307b-127"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="9307b-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9307b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9307b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9307b-129">Übersicht über Syslink-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9307b-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
