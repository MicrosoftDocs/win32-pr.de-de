---
description: Unterklassen werden automatisch Unterklassen und 3D-Effekte zu allen Dialogfeldern in der Anwendung hinzugefügt.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372237"
---
# <a name="ctl3dautosubclass-function"></a><span data-ttu-id="35151-103">Ctl3dAutoSubclass-Funktion</span><span class="sxs-lookup"><span data-stu-id="35151-103">Ctl3dAutoSubclass function</span></span>

<span data-ttu-id="35151-104">Unterklassen werden automatisch Unterklassen und 3D-Effekte zu allen Dialogfeldern in der Anwendung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="35151-104">Automatically subclasses and adds 3D effects to all dialog boxes in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="35151-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35151-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="35151-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35151-107">*hinstapp*</span><span class="sxs-lookup"><span data-stu-id="35151-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="35151-108">Ein Handle für die Anwendung, die als Client registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="35151-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35151-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35151-109">Return value</span></span>

<span data-ttu-id="35151-110">Gibt **true** zurück, es sei denn, eine der folgenden Bedingungen ist vorhanden. in diesem Fall wird **false** zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="35151-110">Returns **TRUE** unless one of the following conditions exists, in which case it returns **FALSE**:</span></span>

-   <span data-ttu-id="35151-111">Ctl3d wird unter Windows, Version 3,0 oder früher, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35151-111">CTL3D is running under Windows version 3.0 or earlier.</span></span>
-   <span data-ttu-id="35151-112">Ctl3d ist in den Tabellen für die aktuelle Anwendung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35151-112">CTL3D does not have space available in its tables for the current application.</span></span> <span data-ttu-id="35151-113">Ctl3d kann bis zu 32 Anwendungen gleichzeitig bedienen.</span><span class="sxs-lookup"><span data-stu-id="35151-113">CTL3D can service up to 32 applications at the same time.</span></span>
-   <span data-ttu-id="35151-114">Ctl3d kann seinen CBT-Hook nicht installieren.</span><span class="sxs-lookup"><span data-stu-id="35151-114">CTL3D cannot install its CBT hook.</span></span>

## <a name="remarks"></a><span data-ttu-id="35151-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35151-115">Remarks</span></span>

<span data-ttu-id="35151-116">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="35151-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="35151-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35151-117">Requirements</span></span>



| <span data-ttu-id="35151-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35151-118">Requirement</span></span> | <span data-ttu-id="35151-119">Wert</span><span class="sxs-lookup"><span data-stu-id="35151-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35151-120">DLL</span><span class="sxs-lookup"><span data-stu-id="35151-120">DLL</span></span><br/> | <dl> <span data-ttu-id="35151-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35151-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
