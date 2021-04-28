---
description: 'pSetupStringTableInitialize-Funktion: Initialisiert eine Zeichenfolgentabelle.'
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize-Funktion
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
ms.openlocfilehash: 79638f9f1f80f4b9b3d54a33c7e94234174ffb19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089199"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="cf4ad-103">pSetupStringTableInitialize-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf4ad-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="cf4ad-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="cf4ad-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="cf4ad-105">Initialisiert eine Zeichenfolgentabelle.</span><span class="sxs-lookup"><span data-stu-id="cf4ad-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4ad-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf4ad-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="cf4ad-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf4ad-107">Parameters</span></span>

<span data-ttu-id="cf4ad-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cf4ad-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4ad-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf4ad-109">Remarks</span></span>

<span data-ttu-id="cf4ad-110">Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cf4ad-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4ad-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf4ad-111">Requirements</span></span>



| <span data-ttu-id="cf4ad-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf4ad-112">Requirement</span></span> | <span data-ttu-id="cf4ad-113">Wert</span><span class="sxs-lookup"><span data-stu-id="cf4ad-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4ad-114">DLL</span><span class="sxs-lookup"><span data-stu-id="cf4ad-114">DLL</span></span><br/> | <dl> <span data-ttu-id="cf4ad-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf4ad-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
