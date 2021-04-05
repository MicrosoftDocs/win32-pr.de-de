---
description: Die isremotenpp-Funktion gibt an, ob das angegebene BLOB eine Remote-NPP angibt.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Isremotenpp-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755392"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="a21a1-103">Isremotenpp-Funktion</span><span class="sxs-lookup"><span data-stu-id="a21a1-103">IsRemoteNPP function</span></span>

<span data-ttu-id="a21a1-104">Die **isremotenpp** -Funktion gibt an, ob das angegebene BLOB eine Remote-NPP angibt.</span><span class="sxs-lookup"><span data-stu-id="a21a1-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a21a1-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="a21a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a21a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21a1-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a21a1-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a21a1-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="a21a1-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21a1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a21a1-109">Return value</span></span>

<span data-ttu-id="a21a1-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="a21a1-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a21a1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a21a1-111">Remarks</span></span>

<span data-ttu-id="a21a1-112">Verwenden Sie diese Funktion, um zu testen, ob eine Remote Kategorie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a21a1-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="a21a1-113">Stellen Sie sicher, dass sich die Namen der Remote Computer und der lokalen Computer unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a21a1-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21a1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a21a1-114">Requirements</span></span>



| <span data-ttu-id="a21a1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a21a1-115">Requirement</span></span> | <span data-ttu-id="a21a1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a21a1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a21a1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a21a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a21a1-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a21a1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a21a1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a21a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a21a1-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a21a1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a21a1-121">Header</span><span class="sxs-lookup"><span data-stu-id="a21a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21a1-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21a1-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a21a1-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a21a1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a21a1-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a21a1-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a21a1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a21a1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a21a1-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a21a1-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




