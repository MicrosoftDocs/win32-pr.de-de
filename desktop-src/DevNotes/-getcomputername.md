---
description: Ruft den Computernamen ab.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: _GetComputerName-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371117"
---
# <a name="_getcomputername-function"></a><span data-ttu-id="62652-103">\_GetComputerName-Funktion</span><span class="sxs-lookup"><span data-stu-id="62652-103">\_GetComputerName function</span></span>

<span data-ttu-id="62652-104">\[Diese Funktion ist ein Wrapper über die **GetComputerName** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="62652-104">\[This function is a wrapper over the **GetComputerName** function.</span></span> <span data-ttu-id="62652-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="62652-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="62652-106">Anwendungen sollten **GetComputerName** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="62652-106">Applications should call **GetComputerName** directly.\]</span></span>

<span data-ttu-id="62652-107">Ruft den Computernamen ab.</span><span class="sxs-lookup"><span data-stu-id="62652-107">Gets the computer name.</span></span> <span data-ttu-id="62652-108">Siehe [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span><span class="sxs-lookup"><span data-stu-id="62652-108">See [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="62652-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="62652-109">Syntax</span></span>


```C++
BOOL _GetComputerName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="62652-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="62652-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62652-111">*...*</span><span class="sxs-lookup"><span data-stu-id="62652-111">*...*</span></span> 
<span data-ttu-id="62652-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="62652-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="62652-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62652-113">Requirements</span></span>



| <span data-ttu-id="62652-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62652-114">Requirement</span></span> | <span data-ttu-id="62652-115">Wert</span><span class="sxs-lookup"><span data-stu-id="62652-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62652-116">DLL</span><span class="sxs-lookup"><span data-stu-id="62652-116">DLL</span></span><br/> | <dl> <span data-ttu-id="62652-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62652-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62652-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62652-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62652-119">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="62652-119">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
