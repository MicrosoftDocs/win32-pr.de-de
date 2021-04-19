---
description: Registriert eine Anwendung als Client von ctl3d.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361652"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="e9d78-103">Ctl3dRegister-Funktion</span><span class="sxs-lookup"><span data-stu-id="e9d78-103">Ctl3dRegister function</span></span>

<span data-ttu-id="e9d78-104">Registriert eine Anwendung als Client von ctl3d.</span><span class="sxs-lookup"><span data-stu-id="e9d78-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9d78-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="e9d78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d78-107">*hinstapp*</span><span class="sxs-lookup"><span data-stu-id="e9d78-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d78-108">Ein Handle für die Anwendung, die als Client registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9d78-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d78-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9d78-109">Return value</span></span>

<span data-ttu-id="e9d78-110">Gibt **true** zurück, wenn 3D-Effekte aktiv sind. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e9d78-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9d78-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9d78-111">Remarks</span></span>

<span data-ttu-id="e9d78-112">Eine Anwendung, die ctl3d verwendet, sollte diese Funktion in WinMain aufruft.</span><span class="sxs-lookup"><span data-stu-id="e9d78-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="e9d78-113">3D-Effekte sind auf Systemen mit einer geringeren Auflösung als VGA nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e9d78-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="e9d78-114">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e9d78-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d78-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9d78-115">Requirements</span></span>



| <span data-ttu-id="e9d78-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9d78-116">Requirement</span></span> | <span data-ttu-id="e9d78-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e9d78-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d78-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e9d78-118">DLL</span></span><br/> | <dl> <span data-ttu-id="e9d78-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d78-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
