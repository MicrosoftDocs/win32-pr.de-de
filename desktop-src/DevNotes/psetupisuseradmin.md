---
description: Gibt an, ob der aktuelle Benutzer ein Administrator ist.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: psetupisuseradmin-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358677"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="7a846-103">psetupisuseradmin-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a846-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="7a846-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="7a846-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="7a846-105">Gibt an, ob der aktuelle Benutzer ein Administrator ist.</span><span class="sxs-lookup"><span data-stu-id="7a846-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a846-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a846-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="7a846-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a846-107">Parameters</span></span>

<span data-ttu-id="7a846-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7a846-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a846-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a846-109">Return value</span></span>

<span data-ttu-id="7a846-110">**True** , wenn der aktuelle Benutzer ein Administrator ist, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7a846-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a846-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a846-111">Remarks</span></span>

<span data-ttu-id="7a846-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a846-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a846-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a846-113">Requirements</span></span>



| <span data-ttu-id="7a846-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a846-114">Requirement</span></span> | <span data-ttu-id="7a846-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7a846-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a846-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7a846-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7a846-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a846-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
