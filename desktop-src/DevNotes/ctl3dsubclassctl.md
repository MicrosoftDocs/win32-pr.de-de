---
description: Unterklassen eines einzelnen Steuer Elements, wenn das Steuerelement nicht in einem Dialogfeld angezeigt wird.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371486"
---
# <a name="ctl3dsubclassctl-function"></a><span data-ttu-id="55b3a-103">Ctl3dSubclassCtl-Funktion</span><span class="sxs-lookup"><span data-stu-id="55b3a-103">Ctl3dSubclassCtl function</span></span>

<span data-ttu-id="55b3a-104">Unterklassen eines einzelnen Steuer Elements, wenn das Steuerelement nicht in einem Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="55b3a-104">Subclasses an individual control unless the control appears in a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55b3a-105">Syntax</span></span>


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="55b3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55b3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b3a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="55b3a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="55b3a-108">Ein Handle für das Steuerelement Fenster.</span><span class="sxs-lookup"><span data-stu-id="55b3a-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b3a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55b3a-109">Return value</span></span>

<span data-ttu-id="55b3a-110">Gibt **true** zurück, wenn das Steuerelement erfolgreich untergeordnet ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="55b3a-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b3a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55b3a-111">Remarks</span></span>

<span data-ttu-id="55b3a-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="55b3a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b3a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55b3a-113">Requirements</span></span>



| <span data-ttu-id="55b3a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55b3a-114">Requirement</span></span> | <span data-ttu-id="55b3a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="55b3a-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b3a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="55b3a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="55b3a-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b3a-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b3a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55b3a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b3a-119">**Ctl3dUnsubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="55b3a-119">**Ctl3dUnsubclassCtl**</span></span>](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
