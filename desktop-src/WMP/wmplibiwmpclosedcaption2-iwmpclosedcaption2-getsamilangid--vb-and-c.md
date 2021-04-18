---
title: IWMPClosedCaption2 getsamilangid-Methode
description: Die getsamilangid-Methode gibt den Gebiets Schema Bezeichner (LCID) einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- getsamilangid-Methode, Windows-Media Player
- getsamilangid-Methode, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface, Windows Media Player, getsamilangid-Methode
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371521"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="70615-106">IWMPClosedCaption2:: getsamilangid-Methode</span><span class="sxs-lookup"><span data-stu-id="70615-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="70615-107">Die **getsamilangid** -Methode gibt den Gebiets Schema Bezeichner (LCID) einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="70615-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="70615-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70615-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="70615-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="70615-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70615-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70615-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70615-111">Ein **System. Int32** -Wert, der der null basierte Index der abzurufenden LCID ist.</span><span class="sxs-lookup"><span data-stu-id="70615-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70615-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70615-112">Return value</span></span>

<span data-ttu-id="70615-113">Ein **System. Int32** , bei dem es sich um die LCID der Sprache mit dem angegebenen Index handelt.</span><span class="sxs-lookup"><span data-stu-id="70615-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="70615-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70615-114">Remarks</span></span>

<span data-ttu-id="70615-115">Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="70615-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="70615-116">Diese Methode gibt 0 zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="70615-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="70615-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70615-117">Requirements</span></span>



| <span data-ttu-id="70615-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70615-118">Requirement</span></span> | <span data-ttu-id="70615-119">Wert</span><span class="sxs-lookup"><span data-stu-id="70615-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70615-120">Version</span><span class="sxs-lookup"><span data-stu-id="70615-120">Version</span></span><br/>   | <span data-ttu-id="70615-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="70615-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="70615-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="70615-122">Namespace</span></span><br/> | <span data-ttu-id="70615-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="70615-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="70615-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="70615-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="70615-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="70615-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70615-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70615-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70615-127">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="70615-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="70615-128">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70615-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="70615-129">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="70615-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





