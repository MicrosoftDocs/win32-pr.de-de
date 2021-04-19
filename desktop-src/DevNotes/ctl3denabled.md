---
description: Überprüft, ob Steuerelemente 3D-Effekte verwenden können.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356036"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="4ce0d-103">Ctl3dEnabled-Funktion</span><span class="sxs-lookup"><span data-stu-id="4ce0d-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="4ce0d-104">Überprüft, ob Steuerelemente 3D-Effekte verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ce0d-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="4ce0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ce0d-106">Parameters</span></span>

<span data-ttu-id="4ce0d-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ce0d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ce0d-108">Return value</span></span>

<span data-ttu-id="4ce0d-109">Gibt **true** zurück, wenn Steuerelemente 3D-Effekte verwenden können. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ce0d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ce0d-110">Remarks</span></span>

<span data-ttu-id="4ce0d-111">In Windows 4,0 oder höher geben **Ctl3dEnabled** und [**Ctl3dRegister**](ctl3dregister.md) **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="4ce0d-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce0d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ce0d-113">Requirements</span></span>



| <span data-ttu-id="4ce0d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ce0d-114">Requirement</span></span> | <span data-ttu-id="4ce0d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4ce0d-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce0d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4ce0d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4ce0d-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ce0d-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
