---
description: Hebt die Registrierung einer Anwendung als Client von ctl3d auf.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365611"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="db473-103">Ctl3dUnregister-Funktion</span><span class="sxs-lookup"><span data-stu-id="db473-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="db473-104">Hebt die Registrierung einer Anwendung als Client von ctl3d auf.</span><span class="sxs-lookup"><span data-stu-id="db473-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="db473-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db473-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="db473-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db473-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db473-107">*hinstapp*</span><span class="sxs-lookup"><span data-stu-id="db473-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="db473-108">Ein Handle für die Anwendung, deren Registrierung als Client aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="db473-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db473-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db473-109">Return value</span></span>

<span data-ttu-id="db473-110">Gibt **true** zurück, wenn die Registrierung der Anwendung als Client von ctl3d aufgehoben wird. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db473-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="db473-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db473-111">Remarks</span></span>

<span data-ttu-id="db473-112">Eine Anwendung, die ctl3d verwendet, sollte diese Funktion in WinMain aufruft.</span><span class="sxs-lookup"><span data-stu-id="db473-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="db473-113">3D-Effekte sind auf Systemen mit einer geringeren Auflösung als VGA nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db473-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="db473-114">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db473-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="db473-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db473-115">Requirements</span></span>



| <span data-ttu-id="db473-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db473-116">Requirement</span></span> | <span data-ttu-id="db473-117">Wert</span><span class="sxs-lookup"><span data-stu-id="db473-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db473-118">DLL</span><span class="sxs-lookup"><span data-stu-id="db473-118">DLL</span></span><br/> | <dl> <span data-ttu-id="db473-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db473-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
