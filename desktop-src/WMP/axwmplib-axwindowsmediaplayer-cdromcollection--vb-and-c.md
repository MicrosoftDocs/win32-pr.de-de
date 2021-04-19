---
title: AxWindowsMediaPlayer. cdromcollection (Eigenschaft)
description: Die cdromcollection-Eigenschaft ruft eine iwmpcdromcollection-Schnittstelle ab, die den Zugriff auf eine Sammlung von CD-oder DVD-Laufwerken ermöglicht.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- cdromcollection-Eigenschaft, Windows-Media Player
- cdromcollection-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, cdromcollection (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367410"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="16006-106">AxWindowsMediaPlayer. cdromcollection (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="16006-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="16006-107">Die cdromcollection-Eigenschaft ruft eine **iwmpcdromcollection** -Schnittstelle ab, die den Zugriff auf eine Sammlung von CD-oder DVD-Laufwerken ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="16006-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="16006-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="16006-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16006-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="16006-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="16006-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="16006-110">Property value</span></span>

<span data-ttu-id="16006-111">Eine WMPLib. iwmpcdromcollection-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="16006-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="16006-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16006-112">Remarks</span></span>

<span data-ttu-id="16006-113">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="16006-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="16006-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="16006-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16006-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16006-115">Requirements</span></span>



| <span data-ttu-id="16006-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16006-116">Requirement</span></span> | <span data-ttu-id="16006-117">Wert</span><span class="sxs-lookup"><span data-stu-id="16006-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16006-118">Version</span><span class="sxs-lookup"><span data-stu-id="16006-118">Version</span></span><br/>   | <span data-ttu-id="16006-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="16006-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="16006-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="16006-120">Namespace</span></span><br/> | <span data-ttu-id="16006-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="16006-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="16006-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="16006-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16006-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="16006-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16006-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16006-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16006-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="16006-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16006-126">**Iwmpcdromcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="16006-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16006-127">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="16006-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16006-128">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="16006-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





