---
description: Deaktiviert die Unterklassen für das angegebene Steuerelement.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354745"
---
# <a name="ctl3dunsubclassctl-function"></a><span data-ttu-id="8921d-103">Ctl3dUnsubclassCtl-Funktion</span><span class="sxs-lookup"><span data-stu-id="8921d-103">Ctl3dUnsubclassCtl function</span></span>

<span data-ttu-id="8921d-104">Deaktiviert die Unterklassen für das angegebene Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8921d-104">Turns off subclassing for the specified control.</span></span>

## <a name="syntax"></a><span data-ttu-id="8921d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8921d-105">Syntax</span></span>


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="8921d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8921d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8921d-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8921d-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8921d-108">Ein Handle für das Steuerelement Fenster.</span><span class="sxs-lookup"><span data-stu-id="8921d-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8921d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8921d-109">Return value</span></span>

<span data-ttu-id="8921d-110">Gibt **true** zurück, wenn das Steuerelement erfolgreich untergeordnet ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8921d-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8921d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8921d-111">Remarks</span></span>

<span data-ttu-id="8921d-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8921d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8921d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8921d-113">Requirements</span></span>



| <span data-ttu-id="8921d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8921d-114">Requirement</span></span> | <span data-ttu-id="8921d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8921d-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8921d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8921d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8921d-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8921d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8921d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8921d-119">**Ctl3dSubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="8921d-119">**Ctl3dSubclassCtl**</span></span>](ctl3dsubclassctl.md)
</dt> </dl>

 

 
