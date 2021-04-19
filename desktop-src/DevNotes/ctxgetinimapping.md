---
description: Bestimmt, ob sich der Terminal Server im Installationsmodus befindet (nur auf Windows-Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Ctxgetinimapping-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370770"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="d0e80-103">Ctxgetinimapping-Funktion</span><span class="sxs-lookup"><span data-stu-id="d0e80-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="d0e80-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0e80-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="d0e80-105">Er kann ohne vorherige Ankündigung geändert oder ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0e80-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="d0e80-106">Verwenden Sie stattdessen **verifyversioninfo**.\]</span><span class="sxs-lookup"><span data-stu-id="d0e80-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="d0e80-107">Bestimmt, ob sich der Terminal Server im Installationsmodus befindet (nur auf Windows-Terminal Server 4,0).</span><span class="sxs-lookup"><span data-stu-id="d0e80-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e80-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0e80-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="d0e80-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0e80-109">Parameters</span></span>

<span data-ttu-id="d0e80-110">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d0e80-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0e80-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0e80-111">Return value</span></span>

<span data-ttu-id="d0e80-112">Diese Funktion gibt **false** zurück, wenn sich der Terminal Server im Installationsmodus befindet, **true** , wenn er sich im Ausführungs Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="d0e80-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e80-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0e80-113">Requirements</span></span>



| <span data-ttu-id="d0e80-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0e80-114">Requirement</span></span> | <span data-ttu-id="d0e80-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d0e80-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e80-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d0e80-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d0e80-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e80-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e80-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0e80-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e80-119">**Verifyversioninfo**</span><span class="sxs-lookup"><span data-stu-id="d0e80-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
