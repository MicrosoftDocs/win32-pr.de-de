---
description: Deaktiviert die automatische unter Klassifizierung.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373956"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="11427-103">Ctl3dUnAutoSubclass-Funktion</span><span class="sxs-lookup"><span data-stu-id="11427-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="11427-104">Deaktiviert die automatische unter Klassifizierung.</span><span class="sxs-lookup"><span data-stu-id="11427-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="11427-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11427-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="11427-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11427-106">Parameters</span></span>

<span data-ttu-id="11427-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="11427-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11427-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11427-108">Return value</span></span>

<span data-ttu-id="11427-109">Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11427-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11427-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11427-110">Remarks</span></span>

<span data-ttu-id="11427-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="11427-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="11427-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11427-112">Requirements</span></span>



| <span data-ttu-id="11427-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11427-113">Requirement</span></span> | <span data-ttu-id="11427-114">Wert</span><span class="sxs-lookup"><span data-stu-id="11427-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11427-115">DLL</span><span class="sxs-lookup"><span data-stu-id="11427-115">DLL</span></span><br/> | <dl> <span data-ttu-id="11427-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11427-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
