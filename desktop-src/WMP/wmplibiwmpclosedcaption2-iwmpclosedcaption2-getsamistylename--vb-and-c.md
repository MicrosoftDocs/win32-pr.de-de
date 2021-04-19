---
title: IWMPClosedCaption2 getsamistylename-Methode
description: Die getsamistylename-Methode gibt den Namen eines Stils zurück, der von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- getsamistylename-Methode, Windows Media Player
- getsamistylename-Methode, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface Windows Media Player, getsamistylename-Methode
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367093"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="8e820-106">IWMPClosedCaption2:: getsamistylename-Methode</span><span class="sxs-lookup"><span data-stu-id="8e820-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="8e820-107">Die **getsamistylename** -Methode gibt den Namen eines Stils zurück, der von der aktuellen Sami-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8e820-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e820-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e820-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="8e820-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e820-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e820-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e820-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e820-111">Ein **System. Int32** -Wert, der der null basierte Index des abzurufenden Format namens ist.</span><span class="sxs-lookup"><span data-stu-id="8e820-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e820-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e820-112">Return value</span></span>

<span data-ttu-id="8e820-113">Eine **System. String** , bei der es sich um den Namen des Stils handelt, der in der Sami-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8e820-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e820-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e820-114">Remarks</span></span>

<span data-ttu-id="8e820-115">Die Stile in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8e820-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="8e820-116">Diese Methode gibt eine Zeichenfolge der Länge 0 (null) zurück (""), es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="8e820-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e820-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e820-117">Requirements</span></span>



| <span data-ttu-id="8e820-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e820-118">Requirement</span></span> | <span data-ttu-id="8e820-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8e820-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e820-120">Version</span><span class="sxs-lookup"><span data-stu-id="8e820-120">Version</span></span><br/>   | <span data-ttu-id="8e820-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="8e820-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8e820-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e820-122">Namespace</span></span><br/> | <span data-ttu-id="8e820-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e820-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8e820-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="8e820-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e820-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e820-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e820-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e820-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e820-127">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="8e820-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8e820-128">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e820-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e820-129">**Iwmpclosedcaption. samistyle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e820-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e820-130">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="8e820-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





