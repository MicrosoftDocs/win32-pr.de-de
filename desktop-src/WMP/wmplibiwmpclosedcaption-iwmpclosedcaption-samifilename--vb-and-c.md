---
title: Iwmpclosedcaption samifilename (Eigenschaft)
description: Die samifilename-Eigenschaft ruft den Namen einer Datei ab, die die für den Untertitel erforderlichen Informationen enthält, oder legt ihn fest.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Samifilename-Eigenschaft, Windows-Media Player
- Samifilename-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, samifilename (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351368"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="01c30-106">Iwmpclosedcaption:: samifilename (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="01c30-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="01c30-107">Die **samifilename** -Eigenschaft ruft den Namen einer Datei ab, die die für den Untertitel erforderlichen Informationen enthält, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="01c30-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c30-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="01c30-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="01c30-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="01c30-109">Property value</span></span>

<span data-ttu-id="01c30-110">" **System. String** " ist der Name der synchronisierten, zugänglichen Medienaustausch Datei (Sami).</span><span class="sxs-lookup"><span data-stu-id="01c30-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c30-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01c30-111">Remarks</span></span>

<span data-ttu-id="01c30-112">Die Sami-Datei muss eine SMI-oder. Sami-Dateinamenerweiterung verwenden.</span><span class="sxs-lookup"><span data-stu-id="01c30-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="01c30-113">Wenn Sie keinen Wert mit **samifilename** festlegen, ruft diese Eigenschaft eine **Zeichenfolge** ab, die den Standard Dateinamen oder die URL enthält, die dem aktuellen Medien Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01c30-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="01c30-114">Diese Zuordnung kann auftreten, wenn eine Sami-Datei mithilfe des *Sami* URL-Parameters angegeben wird, oder automatisch, wenn die Sami-Datei den gleichen Namen wie die digitale Mediendatei hat (mit Ausnahme der Dateinamenerweiterung).</span><span class="sxs-lookup"><span data-stu-id="01c30-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="01c30-115">Wenn dem aktuellen Medium keine Standard-Sami-Datei zugeordnet ist, erhält diese Eigenschaft eine Zeichenfolge der Länge 0 (null) ("").</span><span class="sxs-lookup"><span data-stu-id="01c30-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="01c30-116">Nachdem Sie einen Wert mit **samifilename** festgelegt haben, wird dieser Wert beibehalten, bis Sie einen neuen Wert festlegen (oder bis ein neues Medien Element mithilfe des Sami URL-Parameters geöffnet wird).</span><span class="sxs-lookup"><span data-stu-id="01c30-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="01c30-117">Daher müssen Sie vor jedem neuen Medien Element einen neuen Wert für diese Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="01c30-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="01c30-118">Auf diese Weise wird der neue Wert für **samifilename** wirksam, wenn das nächste Medien Element geöffnet wird (oder wenn **AxWindowsMediaPlayer. Close** aufgerufen wird).</span><span class="sxs-lookup"><span data-stu-id="01c30-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="01c30-119">Das Angeben eines neuen Werts für **samifilename** hat keine Auswirkung auf das aktuelle Medium.</span><span class="sxs-lookup"><span data-stu-id="01c30-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="01c30-120">Legen Sie **samifilename** auf eine Zeichenfolge der Länge 0 ("") fest, bevor Sie das nächste Medien Element wiedergeben, damit Windows Media Player die einem bestimmten Medien Element zugeordnete standardmäßige Sami-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="01c30-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c30-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01c30-121">Requirements</span></span>



| <span data-ttu-id="01c30-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01c30-122">Requirement</span></span> | <span data-ttu-id="01c30-123">Wert</span><span class="sxs-lookup"><span data-stu-id="01c30-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c30-124">Version</span><span class="sxs-lookup"><span data-stu-id="01c30-124">Version</span></span><br/>   | <span data-ttu-id="01c30-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="01c30-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="01c30-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="01c30-126">Namespace</span></span><br/> | <span data-ttu-id="01c30-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="01c30-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="01c30-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="01c30-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="01c30-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="01c30-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c30-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01c30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c30-131">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="01c30-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="01c30-132">**AxWindowsMediaPlayer. Close**</span><span class="sxs-lookup"><span data-stu-id="01c30-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="01c30-133">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="01c30-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="01c30-134">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="01c30-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





