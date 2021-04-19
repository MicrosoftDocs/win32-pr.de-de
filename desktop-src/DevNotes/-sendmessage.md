---
description: Sendet die angegebene Meldung an ein Fenster oder an ein Fenster.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370593"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="d1007-103">\_SendMessage-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1007-103">\_SendMessage function</span></span>

<span data-ttu-id="d1007-104">\[Diese Funktion ist ein Wrapper über die **SendMessage** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d1007-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="d1007-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d1007-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="d1007-106">Anwendungen sollten **SendMessage** direkt aufzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="d1007-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="d1007-107">Sendet die angegebene Meldung an ein Fenster oder an ein Fenster.</span><span class="sxs-lookup"><span data-stu-id="d1007-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="d1007-108">Siehe [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="d1007-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1007-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1007-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="d1007-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1007-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1007-111">*...*</span><span class="sxs-lookup"><span data-stu-id="d1007-111">*...*</span></span> 
<span data-ttu-id="d1007-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d1007-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d1007-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1007-113">Requirements</span></span>



| <span data-ttu-id="d1007-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1007-114">Requirement</span></span> | <span data-ttu-id="d1007-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d1007-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1007-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d1007-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d1007-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1007-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1007-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1007-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1007-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="d1007-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
