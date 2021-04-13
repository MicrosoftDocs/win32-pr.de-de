---
description: Gibt eine Textur frei und benachrichtigt den Host asynchron.
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: fretextureasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aed7d29653b9da6f39b1ef6ec4e600c1857744f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482574"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span data-ttu-id="e0ac9-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: fretextureasync-Methode</span><span class="sxs-lookup"><span data-stu-id="e0ac9-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::FreeTextureAsync method</span></span>

<span data-ttu-id="e0ac9-104">Gibt eine Textur frei und benachrichtigt den Host asynchron.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-104">Frees a texture and notifies the host asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ac9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0ac9-105">Syntax</span></span>


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e0ac9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ac9-106">Parameters</span></span>

<span data-ttu-id="e0ac9-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="e0ac9-107">*textureId* </span></span>  
<span data-ttu-id="e0ac9-108">Die ID der Textur, die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-108">The ID of the texture to free..</span></span>

<span data-ttu-id="e0ac9-109">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="e0ac9-109">*callbacks* </span></span>  
<span data-ttu-id="e0ac9-110">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-110">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="e0ac9-111">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="e0ac9-111">*requestCookie* </span></span>  
<span data-ttu-id="e0ac9-112">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-112">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="e0ac9-113">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="e0ac9-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e0ac9-114">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0ac9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0ac9-115">Return value</span></span>

<span data-ttu-id="e0ac9-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0ac9-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e0ac9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ac9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ac9-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e0ac9-119">Header</span><span class="sxs-lookup"><span data-stu-id="e0ac9-119">Header</span></span></p></td><td><span data-ttu-id="e0ac9-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e0ac9-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e0ac9-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0ac9-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e0ac9-122">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="e0ac9-122">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
