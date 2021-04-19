---
description: Bestimmt, ob sich der Terminal Server im Installationsmodus befindet.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: Termsrvappinstallmode-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373612"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="b1111-103">Termsrvappinstallmode-Funktion</span><span class="sxs-lookup"><span data-stu-id="b1111-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="b1111-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1111-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="b1111-105">Er kann ohne vorherige Ankündigung geändert oder ausgeblendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="b1111-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="b1111-106">Bestimmt, ob sich der Terminal Server im Installationsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="b1111-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1111-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1111-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="b1111-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1111-108">Parameters</span></span>

<span data-ttu-id="b1111-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1111-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1111-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1111-110">Return value</span></span>

<span data-ttu-id="b1111-111">Diese Funktion gibt **true** zurück, wenn sich der Terminal Server im Installationsmodus befindet, und **false** , wenn er sich im Ausführungs Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="b1111-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1111-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1111-112">Requirements</span></span>



| <span data-ttu-id="b1111-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1111-113">Requirement</span></span> | <span data-ttu-id="b1111-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b1111-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1111-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b1111-115">DLL</span></span><br/> | <dl> <span data-ttu-id="b1111-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1111-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




