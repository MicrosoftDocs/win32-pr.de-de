---
description: Ruft den Text aus der Titelleiste des angegebenen Fensters ab.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: _GetWindowText-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372268"
---
# <a name="_getwindowtext-function"></a><span data-ttu-id="bd90d-103">\_GetWindowText-Funktion</span><span class="sxs-lookup"><span data-stu-id="bd90d-103">\_GetWindowText function</span></span>

<span data-ttu-id="bd90d-104">\[Diese Funktion ist ein Wrapper über die **GetWindowText** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bd90d-104">\[This function is a wrapper over the **GetWindowText** function.</span></span> <span data-ttu-id="bd90d-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bd90d-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="bd90d-106">Anwendungen sollten **GetWindowText** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="bd90d-106">Applications should call **GetWindowText** directly.\]</span></span>

<span data-ttu-id="bd90d-107">Ruft den Text aus der Titelleiste des angegebenen Fensters ab.</span><span class="sxs-lookup"><span data-stu-id="bd90d-107">Retrieves the text from the specified window's title bar.</span></span> <span data-ttu-id="bd90d-108">Weitere Informationen finden Sie unter [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="bd90d-108">See [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd90d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd90d-109">Syntax</span></span>


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="bd90d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd90d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd90d-111">*...*</span><span class="sxs-lookup"><span data-stu-id="bd90d-111">*...*</span></span> 
<span data-ttu-id="bd90d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bd90d-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bd90d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd90d-113">Requirements</span></span>



| <span data-ttu-id="bd90d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd90d-114">Requirement</span></span> | <span data-ttu-id="bd90d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bd90d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd90d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="bd90d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="bd90d-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd90d-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd90d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd90d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd90d-119">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="bd90d-119">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
