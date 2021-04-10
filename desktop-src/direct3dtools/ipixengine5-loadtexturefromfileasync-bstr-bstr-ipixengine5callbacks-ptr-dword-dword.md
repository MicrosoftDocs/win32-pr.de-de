---
description: Lädt eine Textur aus einer Datei und benachrichtigt den Host beim Abschluss asynchron.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: loadtexturefromfileasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125378"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="580b7-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: loadtexturefromfileasync-Methode</span><span class="sxs-lookup"><span data-stu-id="580b7-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="580b7-104">Lädt eine Textur aus einer Datei und benachrichtigt den Host beim Abschluss asynchron.</span><span class="sxs-lookup"><span data-stu-id="580b7-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="580b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="580b7-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="580b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="580b7-106">Parameters</span></span>

<span data-ttu-id="580b7-107">*Einfügen* </span><span class="sxs-lookup"><span data-stu-id="580b7-107">*fileName* </span></span>  
<span data-ttu-id="580b7-108">Eine com-Zeichenfolge, die den Namen der Textur Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="580b7-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="580b7-109">*histogrammdatafilename* </span><span class="sxs-lookup"><span data-stu-id="580b7-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="580b7-110">Eine com-Zeichenfolge mit dem Namen der histogrammdatendatei, die der Textur zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="580b7-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="580b7-111">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="580b7-111">*callbacks* </span></span>  
<span data-ttu-id="580b7-112">Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="580b7-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="580b7-113">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="580b7-113">*requestCookie* </span></span>  
<span data-ttu-id="580b7-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="580b7-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="580b7-115">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="580b7-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="580b7-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="580b7-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="580b7-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="580b7-117">Return value</span></span>

<span data-ttu-id="580b7-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="580b7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="580b7-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="580b7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="580b7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="580b7-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="580b7-121">Header</span><span class="sxs-lookup"><span data-stu-id="580b7-121">Header</span></span></p></td><td><span data-ttu-id="580b7-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="580b7-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="580b7-123"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="580b7-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="580b7-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="580b7-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
