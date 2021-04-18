---
title: AxWindowsMediaPlayer. newmedia-Methode
description: Die newmedia-Methode gibt eine iwmpmedia-Schnittstelle für ein neues Medien Element zurück.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- newmedia-Methode, Windows-Media Player
- newmedia-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, newmedia-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365492"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="0fcdd-106">AxWindowsMediaPlayer. newmedia-Methode</span><span class="sxs-lookup"><span data-stu-id="0fcdd-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="0fcdd-107">Die newmedia-Methode gibt eine iwmpmedia-Schnittstelle für ein neues Medien Element zurück.</span><span class="sxs-lookup"><span data-stu-id="0fcdd-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fcdd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fcdd-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="0fcdd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fcdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fcdd-110">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="0fcdd-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="0fcdd-111">Ein **System. String** -Wert, der die URL der digitalen Mediendatei ist, die zum Initialisieren des neuen Medien Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fcdd-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fcdd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fcdd-112">Return value</span></span>

<span data-ttu-id="0fcdd-113">Eine WMPLib. iwmpmedia-Schnittstelle, die das neu erstellte Medien Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fcdd-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fcdd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fcdd-114">Remarks</span></span>

<span data-ttu-id="0fcdd-115">Der *bstrinurl* -Parameter darf keine Zeichenfolge der Länge 0 ("") oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0fcdd-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fcdd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fcdd-116">Requirements</span></span>



| <span data-ttu-id="0fcdd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fcdd-117">Requirement</span></span> | <span data-ttu-id="0fcdd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0fcdd-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fcdd-119">Version</span><span class="sxs-lookup"><span data-stu-id="0fcdd-119">Version</span></span><br/>   | <span data-ttu-id="0fcdd-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0fcdd-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0fcdd-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0fcdd-121">Namespace</span></span><br/> | <span data-ttu-id="0fcdd-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0fcdd-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0fcdd-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="0fcdd-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0fcdd-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0fcdd-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fcdd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fcdd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fcdd-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0fcdd-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0fcdd-127">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0fcdd-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





