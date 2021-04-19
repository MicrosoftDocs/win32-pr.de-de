---
description: Initialisiert eine Zeichen folgen Tabelle.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: psetupstringtableinitialize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369964"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="22fbd-103">psetupstringtableinitialize-Funktion</span><span class="sxs-lookup"><span data-stu-id="22fbd-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="22fbd-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="22fbd-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="22fbd-105">Initialisiert eine Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="22fbd-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="22fbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="22fbd-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="22fbd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22fbd-107">Parameters</span></span>

<span data-ttu-id="22fbd-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="22fbd-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="22fbd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22fbd-109">Remarks</span></span>

<span data-ttu-id="22fbd-110">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22fbd-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="22fbd-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22fbd-111">Requirements</span></span>



| <span data-ttu-id="22fbd-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22fbd-112">Requirement</span></span> | <span data-ttu-id="22fbd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="22fbd-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22fbd-114">DLL</span><span class="sxs-lookup"><span data-stu-id="22fbd-114">DLL</span></span><br/> | <dl> <span data-ttu-id="22fbd-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22fbd-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
