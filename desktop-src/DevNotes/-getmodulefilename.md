---
description: Ruft den Modulpfad ab.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373950"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="a0dfb-103">\_GetModuleFileName-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0dfb-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="a0dfb-104">\[Diese Funktion ist ein Wrapper über die **GetModuleFileName** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a0dfb-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="a0dfb-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="a0dfb-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="a0dfb-106">Anwendungen sollten **GetModuleFileName** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="a0dfb-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="a0dfb-107">Ruft den Modulpfad ab.</span><span class="sxs-lookup"><span data-stu-id="a0dfb-107">Gets the module path.</span></span> <span data-ttu-id="a0dfb-108">Siehe [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span><span class="sxs-lookup"><span data-stu-id="a0dfb-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0dfb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0dfb-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="a0dfb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0dfb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0dfb-111">*...*</span><span class="sxs-lookup"><span data-stu-id="a0dfb-111">*...*</span></span> 
<span data-ttu-id="a0dfb-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a0dfb-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a0dfb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0dfb-113">Requirements</span></span>



| <span data-ttu-id="a0dfb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0dfb-114">Requirement</span></span> | <span data-ttu-id="a0dfb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a0dfb-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dfb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a0dfb-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a0dfb-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0dfb-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0dfb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0dfb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0dfb-119">**Fehler bei GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="a0dfb-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
