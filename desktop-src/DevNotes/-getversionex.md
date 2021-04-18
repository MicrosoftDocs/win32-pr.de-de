---
description: Ruft Informationen zur Betriebssystemversion ab.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372269"
---
# <a name="_getversionex-function"></a><span data-ttu-id="4f408-103">\_GetVersionEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="4f408-103">\_GetVersionEx function</span></span>

<span data-ttu-id="4f408-104">\[Diese Funktion ist ein Wrapper über die **GetVersionEx** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4f408-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="4f408-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="4f408-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="4f408-106">Anwendungen sollten **GetVersionEx** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="4f408-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="4f408-107">Ruft Informationen zur Betriebssystemversion ab.</span><span class="sxs-lookup"><span data-stu-id="4f408-107">Gets information about the operating system version.</span></span> <span data-ttu-id="4f408-108">Siehe [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span><span class="sxs-lookup"><span data-stu-id="4f408-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f408-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f408-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="4f408-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f408-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f408-111">*...*</span><span class="sxs-lookup"><span data-stu-id="4f408-111">*...*</span></span> 
<span data-ttu-id="4f408-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4f408-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4f408-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f408-113">Requirements</span></span>



| <span data-ttu-id="4f408-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f408-114">Requirement</span></span> | <span data-ttu-id="4f408-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4f408-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f408-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4f408-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4f408-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f408-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f408-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f408-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f408-119">**GetVersionEx**</span><span class="sxs-lookup"><span data-stu-id="4f408-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
