---
description: Speichert eine Textur.
MS-HAID: vspixengine.IPixEngine5\_SaveTextureAsync\_UINT\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: savetextureasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6F08F49E-6FFD-4A9B-86F5-8CB499947F57
api_name:
- IPixEngine5.SaveTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2590f793d0ba05af1ccf9e10ba04fa8b6aa2421b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482635"
---
# <a name="span-idvspixengineipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5savetextureasync-method"></a><span data-ttu-id="c26ed-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: savetextureasync-Methode</span><span class="sxs-lookup"><span data-stu-id="c26ed-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::SaveTextureAsync method</span></span>

<span data-ttu-id="c26ed-104">Speichert eine Textur.</span><span class="sxs-lookup"><span data-stu-id="c26ed-104">Saves a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c26ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c26ed-105">Syntax</span></span>


```C++
HRESULT SaveTextureAsync(
   UINT                  textureId,
   BSTR                  fileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c26ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c26ed-106">Parameters</span></span>

<span data-ttu-id="c26ed-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="c26ed-107">*textureId* </span></span>  
<span data-ttu-id="c26ed-108">Die ID der zu speichernden Textur.</span><span class="sxs-lookup"><span data-stu-id="c26ed-108">The ID of the texture to save.</span></span>

<span data-ttu-id="c26ed-109">*Einfügen* </span><span class="sxs-lookup"><span data-stu-id="c26ed-109">*fileName* </span></span>  
<span data-ttu-id="c26ed-110">Eine com-Zeichenfolge, die den Pfadnamen der gespeicherten Textur enthält.</span><span class="sxs-lookup"><span data-stu-id="c26ed-110">A COM string containing the pathname of the saved texture.</span></span>

<span data-ttu-id="c26ed-111">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="c26ed-111">*callbacks* </span></span>  
<span data-ttu-id="c26ed-112">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c26ed-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="c26ed-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="c26ed-113">*requestCookie* </span></span>  
<span data-ttu-id="c26ed-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c26ed-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c26ed-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="c26ed-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c26ed-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c26ed-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c26ed-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c26ed-117">Return value</span></span>

<span data-ttu-id="c26ed-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c26ed-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c26ed-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c26ed-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26ed-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c26ed-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c26ed-121">Header</span><span class="sxs-lookup"><span data-stu-id="c26ed-121">Header</span></span></p></td><td><span data-ttu-id="c26ed-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c26ed-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c26ed-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c26ed-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c26ed-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="c26ed-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
