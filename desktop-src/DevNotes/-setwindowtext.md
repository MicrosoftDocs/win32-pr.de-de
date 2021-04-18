---
description: Ändert den Text der Titelleiste des angegebenen Fensters (sofern eine solche).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365630"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="5f609-103">\_SetWindowText-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f609-103">\_SetWindowText function</span></span>

<span data-ttu-id="5f609-104">\[Diese Funktion ist ein Wrapper über die **SetWindowText** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5f609-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="5f609-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="5f609-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="5f609-106">Anwendungen sollten **SetWindowText** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="5f609-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="5f609-107">Ändert den Text der Titelleiste des angegebenen Fensters (sofern eine solche).</span><span class="sxs-lookup"><span data-stu-id="5f609-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="5f609-108">Siehe [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="5f609-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f609-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f609-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="5f609-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f609-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f609-111">*...*</span><span class="sxs-lookup"><span data-stu-id="5f609-111">*...*</span></span> 
<span data-ttu-id="5f609-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5f609-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5f609-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f609-113">Requirements</span></span>



| <span data-ttu-id="5f609-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f609-114">Requirement</span></span> | <span data-ttu-id="5f609-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f609-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f609-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5f609-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5f609-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f609-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f609-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f609-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f609-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="5f609-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
