---
description: Überprüft, ob der Medienbereich im DVD-Laufwerk mit dem DVD-Laufwerks Bereich übereinstimmt.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DVDLauncher-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127292"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="6c6d1-103">DVDLauncher-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c6d1-103">DvdLauncher function</span></span>

<span data-ttu-id="6c6d1-104">Überprüft, ob der Medienbereich im DVD-Laufwerk mit dem DVD-Laufwerks Bereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6c6d1-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c6d1-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="6c6d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c6d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6d1-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c6d1-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6d1-108">Ein Handle für das Fenster auf oberster Ebene, das für jede erforderliche Benutzeroberfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c6d1-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="6c6d1-109">Laufwerk *Etter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c6d1-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6d1-110">Der Laufwerk Buchstabe.</span><span class="sxs-lookup"><span data-stu-id="6c6d1-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6d1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c6d1-111">Return value</span></span>

<span data-ttu-id="6c6d1-112">Wenn die Funktion erfolgreich ausgeführt wird und die Bereiche einander entsprechen, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6c6d1-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="6c6d1-113">Andernfalls ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6c6d1-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6d1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c6d1-114">Remarks</span></span>

<span data-ttu-id="6c6d1-115">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="6c6d1-115">This function has no associated import library.</span></span> <span data-ttu-id="6c6d1-116">Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit StorProp.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6c6d1-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6d1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c6d1-117">Requirements</span></span>



| <span data-ttu-id="6c6d1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c6d1-118">Requirement</span></span> | <span data-ttu-id="6c6d1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6c6d1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6d1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c6d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6d1-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c6d1-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6c6d1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c6d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6d1-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c6d1-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6c6d1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6d1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c6d1-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6d1-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6d1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c6d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6d1-127">Geräte Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="6c6d1-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

