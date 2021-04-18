---
description: Diese Funktion Ruft die Version der Offline Registrierungs Bibliothek ab.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Orgetversion-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371128"
---
# <a name="orgetversion-function"></a><span data-ttu-id="98c92-103">Orgetversion-Funktion</span><span class="sxs-lookup"><span data-stu-id="98c92-103">ORGetVersion function</span></span>

<span data-ttu-id="98c92-104">Diese Funktion Ruft die Version der Offline Registrierungs Bibliothek ab.</span><span class="sxs-lookup"><span data-stu-id="98c92-104">This function retrieves the version of the offline registry library.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98c92-105">Syntax</span></span>


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="98c92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c92-107">*pdwmajorversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98c92-107">*pdwMajorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98c92-108">Ein Zeiger auf eine Variable, um die Hauptversion der Offline Registrierungs Bibliothek zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98c92-108">A pointer to a variable to receive the major version of the offline registry library.</span></span> <span data-ttu-id="98c92-109">Bei der ersten Veröffentlichung der Bibliothek ist der Wert 1.</span><span class="sxs-lookup"><span data-stu-id="98c92-109">For the initial release of the library, the value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="98c92-110">*pdwminorversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98c92-110">*pdwMinorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98c92-111">Ein Zeiger auf eine Variable, um die neben Version der Offline Registrierungs Bibliothek zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98c92-111">A pointer to a variable to receive the minor version of the offline registry library.</span></span> <span data-ttu-id="98c92-112">Bei der ersten Veröffentlichung der Bibliothek ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="98c92-112">For the initial release of the library, the value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c92-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98c92-113">Return value</span></span>

<span data-ttu-id="98c92-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="98c92-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c92-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98c92-115">Requirements</span></span>



| <span data-ttu-id="98c92-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98c92-116">Requirement</span></span> | <span data-ttu-id="98c92-117">Wert</span><span class="sxs-lookup"><span data-stu-id="98c92-117">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98c92-118">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="98c92-118">Redistributable</span></span><br/> | <span data-ttu-id="98c92-119">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="98c92-119">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="98c92-120">Header</span><span class="sxs-lookup"><span data-stu-id="98c92-120">Header</span></span><br/>          | <dl> <span data-ttu-id="98c92-121"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c92-121"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="98c92-122">DLL</span><span class="sxs-lookup"><span data-stu-id="98c92-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="98c92-123"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98c92-123"><dt>Offreg.dll</dt></span></span> </dl> |



 

 




