---
title: AxWindowsMediaPlayer. openplayer-Methode
description: Die openplayer-Methode öffnet Windows Media Player unter Verwendung der angegebenen URL. | AxWindowsMediaPlayer. openplayer-Methode
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- openplayer-Methode, Windows-Media Player
- openplayer-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, openplayer-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358291"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="ecf2d-107">AxWindowsMediaPlayer. openplayer-Methode</span><span class="sxs-lookup"><span data-stu-id="ecf2d-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="ecf2d-108">Die **openplayer** -Methode öffnet Windows Media Player unter Verwendung der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf2d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecf2d-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="ecf2d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecf2d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf2d-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="ecf2d-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf2d-112">Die **System. String** -URL, die die URL des wieder zugebende Medien Elements ist.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf2d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecf2d-113">Return value</span></span>

<span data-ttu-id="ecf2d-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf2d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecf2d-115">Remarks</span></span>

<span data-ttu-id="ecf2d-116">Mit dieser Methode wird Windows Media Player gestartet, wobei der angegebene URL als Aktuelles Medien Element festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="ecf2d-117">Wenn der Spieler zuvor im Skin-Modus geschlossen wurde, wird er mithilfe der Skin geöffnet, die zuletzt vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="ecf2d-118">Andernfalls wird der Spieler im vollständigen Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ecf2d-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf2d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecf2d-119">Requirements</span></span>



| <span data-ttu-id="ecf2d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecf2d-120">Requirement</span></span> | <span data-ttu-id="ecf2d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ecf2d-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf2d-122">Version</span><span class="sxs-lookup"><span data-stu-id="ecf2d-122">Version</span></span><br/>   | <span data-ttu-id="ecf2d-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ecf2d-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ecf2d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ecf2d-124">Namespace</span></span><br/> | <span data-ttu-id="ecf2d-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ecf2d-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ecf2d-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="ecf2d-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ecf2d-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ecf2d-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf2d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecf2d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf2d-129">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ecf2d-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





