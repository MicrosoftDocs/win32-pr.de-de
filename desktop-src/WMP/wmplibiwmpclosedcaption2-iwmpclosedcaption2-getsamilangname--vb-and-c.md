---
title: IWMPClosedCaption2 getsamilangname-Methode
description: Die getsamilangname-Methode gibt den Namen einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- getsamilangname-Methode, Windows Media Player
- getsamilangname-Methode, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface Windows Media Player, getsamilangname-Methode
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367094"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="f72a2-106">IWMPClosedCaption2:: getsamilangname-Methode</span><span class="sxs-lookup"><span data-stu-id="f72a2-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="f72a2-107">Die **getsamilangname** -Methode gibt den Namen einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f72a2-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72a2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f72a2-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="f72a2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f72a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72a2-110">*nIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f72a2-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72a2-111">**Ein System. Int32** -Wert, der der null basierte Index des abzurufenden sprach namens ist.</span><span class="sxs-lookup"><span data-stu-id="f72a2-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72a2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f72a2-112">Return value</span></span>

<span data-ttu-id="f72a2-113">Eine **System. String** , bei der es sich um den Namen der Sprache handelt, wie in der Sami-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="f72a2-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="f72a2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f72a2-114">Remarks</span></span>

<span data-ttu-id="f72a2-115">Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f72a2-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="f72a2-116">Diese Methode gibt eine Zeichenfolge der Länge 0 (null) zurück (""), es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="f72a2-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="f72a2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f72a2-117">Requirements</span></span>



| <span data-ttu-id="f72a2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f72a2-118">Requirement</span></span> | <span data-ttu-id="f72a2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f72a2-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72a2-120">Version</span><span class="sxs-lookup"><span data-stu-id="f72a2-120">Version</span></span><br/>   | <span data-ttu-id="f72a2-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f72a2-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f72a2-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f72a2-122">Namespace</span></span><br/> | <span data-ttu-id="f72a2-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f72a2-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f72a2-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="f72a2-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f72a2-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f72a2-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72a2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f72a2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72a2-127">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="f72a2-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f72a2-128">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f72a2-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f72a2-129">**Iwmpclosedcaption. samilang (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f72a2-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f72a2-130">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f72a2-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





