---
description: Gibt eine partielle Sperre frei, sodass andere exklusive oder partielle sperrenerwerber jetzt eingeben können.
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: Csharelocknh::P artialunlock-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368496"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="cea20-103">Csharelocknh::P artialunlock-Methode</span><span class="sxs-lookup"><span data-stu-id="cea20-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="cea20-104">Gibt eine partielle Sperre frei, sodass andere exklusive oder partielle sperrenerwerber jetzt eingeben können.</span><span class="sxs-lookup"><span data-stu-id="cea20-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cea20-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="cea20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cea20-106">Parameters</span></span>

<span data-ttu-id="cea20-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cea20-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cea20-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cea20-108">Return value</span></span>

<span data-ttu-id="cea20-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cea20-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea20-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cea20-110">Remarks</span></span>

<span data-ttu-id="cea20-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cea20-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea20-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cea20-112">Requirements</span></span>



| <span data-ttu-id="cea20-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cea20-113">Requirement</span></span> | <span data-ttu-id="cea20-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cea20-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cea20-115">DLL</span><span class="sxs-lookup"><span data-stu-id="cea20-115">DLL</span></span><br/> | <dl> <span data-ttu-id="cea20-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cea20-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
