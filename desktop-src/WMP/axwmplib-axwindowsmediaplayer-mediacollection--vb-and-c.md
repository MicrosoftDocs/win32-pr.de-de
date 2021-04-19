---
title: AxWindowsMediaPlayer. mediacollection (Eigenschaft)
description: Die mediacollection-Eigenschaft ruft eine iwmpmediacollection-Schnittstelle ab, die eine Möglichkeit bietet, eine große Sammlung von Medien Elementen zu organisieren.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- mediacollection-Eigenschaft, Windows-Media Player
- mediacollection-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, mediacollection (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359746"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="b0a80-106">AxWindowsMediaPlayer. mediacollection (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b0a80-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="b0a80-107">Die mediacollection-Eigenschaft ruft eine **iwmpmediacollection** -Schnittstelle ab, die eine Möglichkeit bietet, eine große Sammlung von Medien Elementen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="b0a80-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="b0a80-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b0a80-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a80-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0a80-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="b0a80-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b0a80-110">Property value</span></span>

<span data-ttu-id="b0a80-111">Die WMPLib. iwmpmediacollection-Schnittstelle zu einer Auflistung von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="b0a80-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a80-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0a80-112">Remarks</span></span>

<span data-ttu-id="b0a80-113">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b0a80-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="b0a80-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b0a80-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a80-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0a80-115">Requirements</span></span>



| <span data-ttu-id="b0a80-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0a80-116">Requirement</span></span> | <span data-ttu-id="b0a80-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b0a80-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a80-118">Version</span><span class="sxs-lookup"><span data-stu-id="b0a80-118">Version</span></span><br/>   | <span data-ttu-id="b0a80-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b0a80-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b0a80-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0a80-120">Namespace</span></span><br/> | <span data-ttu-id="b0a80-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b0a80-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b0a80-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="b0a80-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b0a80-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b0a80-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0a80-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a80-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a80-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b0a80-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0a80-126">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b0a80-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0a80-127">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b0a80-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0a80-128">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b0a80-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





