---
description: Erhält exklusiv eine Sperre, wenn Sie zurzeit nicht von anderen Benutzern gespeichert wird.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'Csharelocknh:: tryexclusivelock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359340"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="35005-103">Csharelocknh:: tryexclusivelock-Methode</span><span class="sxs-lookup"><span data-stu-id="35005-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="35005-104">Erhält exklusiv eine Sperre, wenn Sie zurzeit nicht von anderen Benutzern gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="35005-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="35005-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35005-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="35005-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35005-106">Parameters</span></span>

<span data-ttu-id="35005-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="35005-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35005-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35005-108">Return value</span></span>

<span data-ttu-id="35005-109">Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35005-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="35005-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35005-110">Remarks</span></span>

<span data-ttu-id="35005-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="35005-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="35005-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35005-112">Requirements</span></span>



| <span data-ttu-id="35005-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35005-113">Requirement</span></span> | <span data-ttu-id="35005-114">Wert</span><span class="sxs-lookup"><span data-stu-id="35005-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35005-115">DLL</span><span class="sxs-lookup"><span data-stu-id="35005-115">DLL</span></span><br/> | <dl> <span data-ttu-id="35005-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35005-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
