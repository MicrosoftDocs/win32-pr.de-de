---
title: Media. getiteminfo-Methode
description: Die getiteminfo-Methode ruft den Wert des angegebenen Attributs für das aktuelle Medien Element ab.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361696"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="f2461-106">Media. getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="f2461-106">Media.getItemInfo method</span></span>

<span data-ttu-id="f2461-107">Die **getiteminfo** -Methode ruft den Wert des angegebenen Attributs für das aktuelle Medien Element ab.</span><span class="sxs-lookup"><span data-stu-id="f2461-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2461-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2461-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="f2461-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2461-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2461-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2461-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2461-111">**Zeichenfolge** , die den Namen des Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="f2461-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="f2461-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="f2461-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2461-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2461-113">Return value</span></span>

<span data-ttu-id="f2461-114">Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2461-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="f2461-115">Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2461-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="f2461-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2461-116">Remarks</span></span>

<span data-ttu-id="f2461-117">Diese Methode ruft die Metadaten für ein einzelnes digitales Medien Element oder ein Medien Element ab, das Teil einer Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="f2461-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="f2461-118">Die **AttributeCount** -Eigenschaft enthält die Anzahl von Attributnamen, die für ein bestimmtes **Medien** Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f2461-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="f2461-119">Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f2461-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="f2461-120">Einzelne Attributnamen können an **getiteminfo** übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="f2461-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="f2461-121">Um Attribute mit mehreren Werten und Attributen mit komplexen Werten abzurufen, verwenden Sie die **getItemInfoByType** -Methode.</span><span class="sxs-lookup"><span data-stu-id="f2461-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="f2461-122">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2461-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f2461-123">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f2461-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f2461-124">Zum Freigeben der Windows Media-Bibliotheken über UPnP erstellt Windows Media Player einen Inhaltsverzeichnis Dienst (CDs), der über UPnP verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="f2461-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="f2461-125">Andere Geräte können dann navigieren und die Bibliotheken durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="f2461-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="f2461-126">In Windows 7 kann eine Anwendung die Attribute "Windows Media Player [**trackingID**](trackingid-attribute.md) " und " [**mediaType**](mediatype-attribute.md) " verwenden, um die Objekt-ID der einzelnen Elemente in den CDs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2461-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="f2461-127">Beachten Sie, dass sich diese Konstruktion in zukünftigen Versionen von Windows ändern kann.</span><span class="sxs-lookup"><span data-stu-id="f2461-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="f2461-128">Die Anwendung übergibt jede dieser Attribut Zeichenfolgen im *Name* -Parameter in einem Aufrufen von **getiteminfo**.</span><span class="sxs-lookup"><span data-stu-id="f2461-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="f2461-129">**getiteminfo** gibt den Wert für jedes Attribut im Rückgabewert zurück.</span><span class="sxs-lookup"><span data-stu-id="f2461-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="f2461-130">Die Anwendung verwendet dann die folgende Syntax, um jede Objekt-ID zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f2461-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="f2461-131">*TrackingID*. 0. *Mediatypeid*</span><span class="sxs-lookup"><span data-stu-id="f2461-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="f2461-132">Diese Syntax hat die folgende Bedeutung:</span><span class="sxs-lookup"><span data-stu-id="f2461-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="f2461-133">*TrackingID* ist die Zeichenfolge, die im Windows Media Player [**trackingID**](trackingid-attribute.md) -Attribut des Medien Elements gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f2461-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="f2461-134">*Mediatypeid* hängt vom Wert des [**mediaType**](mediatype-attribute.md) -Attributs ab, wie in der folgenden Tabelle gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f2461-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="f2461-135">MediaType-Attribut</span><span class="sxs-lookup"><span data-stu-id="f2461-135">MediaType attribute</span></span>                      | <span data-ttu-id="f2461-136">Mediatypeid</span><span class="sxs-lookup"><span data-stu-id="f2461-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="f2461-137">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="f2461-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="f2461-138">4</span><span class="sxs-lookup"><span data-stu-id="f2461-138">4</span></span>           |
    | [<span data-ttu-id="f2461-139">Foto Elemente</span><span class="sxs-lookup"><span data-stu-id="f2461-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="f2461-140">B</span><span class="sxs-lookup"><span data-stu-id="f2461-140">B</span></span>           |
    | [<span data-ttu-id="f2461-141">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="f2461-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="f2461-142">8</span><span class="sxs-lookup"><span data-stu-id="f2461-142">8</span></span>           |

    

     

<span data-ttu-id="f2461-143">**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f2461-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2461-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2461-144">Requirements</span></span>



| <span data-ttu-id="f2461-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2461-145">Requirement</span></span> | <span data-ttu-id="f2461-146">Wert</span><span class="sxs-lookup"><span data-stu-id="f2461-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2461-147">Version</span><span class="sxs-lookup"><span data-stu-id="f2461-147">Version</span></span><br/> | <span data-ttu-id="f2461-148">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="f2461-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f2461-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f2461-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="f2461-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2461-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2461-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2461-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2461-152">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="f2461-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f2461-153">**Media. AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="f2461-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="f2461-154">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="f2461-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="f2461-155">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="f2461-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="f2461-156">**"Media. mentiteminfo"**</span><span class="sxs-lookup"><span data-stu-id="f2461-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="f2461-157">**Lesen von Attributwerten**</span><span class="sxs-lookup"><span data-stu-id="f2461-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="f2461-158">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="f2461-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f2461-159">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="f2461-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





