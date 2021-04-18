---
description: Gibt die Version von ctl3d an, die zurzeit ausgeführt wird.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365745"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="a58b9-103">Ctl3dGetVer-Funktion</span><span class="sxs-lookup"><span data-stu-id="a58b9-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="a58b9-104">Gibt die Version von ctl3d an, die zurzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a58b9-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="a58b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a58b9-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="a58b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a58b9-106">Parameters</span></span>

<span data-ttu-id="a58b9-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a58b9-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a58b9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a58b9-108">Return value</span></span>

<span data-ttu-id="a58b9-109">Gibt einen-Wert zurück, der die Hauptversionsnummer im Byte mit hoher Reihenfolge und die neben Versionsnummer im nieder wertigen Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="a58b9-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="a58b9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a58b9-110">Remarks</span></span>

<span data-ttu-id="a58b9-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a58b9-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a58b9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a58b9-112">Requirements</span></span>



| <span data-ttu-id="a58b9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a58b9-113">Requirement</span></span> | <span data-ttu-id="a58b9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a58b9-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a58b9-115">DLL</span><span class="sxs-lookup"><span data-stu-id="a58b9-115">DLL</span></span><br/> | <dl> <span data-ttu-id="a58b9-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a58b9-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
