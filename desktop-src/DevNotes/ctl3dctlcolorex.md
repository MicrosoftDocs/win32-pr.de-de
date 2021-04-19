---
description: Behandelt die WM \_ CtlColor-Meldung für Anwendungen, die ctl3d verwenden.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373935"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="94d19-103">Ctl3dCtlColorEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="94d19-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="94d19-104">Behandelt die **WM \_ CtlColor** -Meldung für Anwendungen, die ctl3d verwenden.</span><span class="sxs-lookup"><span data-stu-id="94d19-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94d19-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="94d19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="94d19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d19-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="94d19-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="94d19-108">Die **WM- \_ CtlColor** -Meldung für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="94d19-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="94d19-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94d19-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d19-110">Ein Handle für den Anzeige Kontext (DC).</span><span class="sxs-lookup"><span data-stu-id="94d19-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="94d19-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94d19-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d19-112">Ein Handle für ein untergeordnetes Fenster (-Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="94d19-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d19-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94d19-113">Return value</span></span>

<span data-ttu-id="94d19-114">Gibt ein Handle für den passenden Pinsel zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird zurück `(HBRUSH)(0)` gegeben, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="94d19-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="94d19-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94d19-115">Remarks</span></span>

<span data-ttu-id="94d19-116">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="94d19-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d19-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94d19-117">Requirements</span></span>



| <span data-ttu-id="94d19-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94d19-118">Requirement</span></span> | <span data-ttu-id="94d19-119">Wert</span><span class="sxs-lookup"><span data-stu-id="94d19-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d19-120">DLL</span><span class="sxs-lookup"><span data-stu-id="94d19-120">DLL</span></span><br/> | <dl> <span data-ttu-id="94d19-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d19-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
