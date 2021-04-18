---
title: Extern. changeviewonlinelist-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. changeviewonlinelist-Methode
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- changeviewonlinelist-Methode, Windows Media Player
- changeviewonlinelist-Methode, Windows Media Player, externe Klasse
- Externe Klasse Windows Media Player, changeviewonlinelist-Methode
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358695"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="bd4d3-107">Extern. changeviewonlinelist-Methode</span><span class="sxs-lookup"><span data-stu-id="bd4d3-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="bd4d3-108">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="bd4d3-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bd4d3-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bd4d3-110">Die **changeviewonlinelist** -Methode ändert die Ansicht in Windows Media Player, um eine Liste anzuzeigen, die dynamisch vom Online Store generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd4d3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd4d3-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="bd4d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd4d3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd4d3-113">*Librarylocationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd4d3-114">Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ der neuen Ansicht angibt.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="bd4d3-115">Beispielsweise gibt die Konstante cpgenreid an, dass in der neuen Ansicht ein bestimmtes Genre angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="bd4d3-116">*Librarylocationid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd4d3-117">**Zeichenfolge** , die die ID des bestimmten Elements enthält, das in der neuen Ansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="bd4d3-118">Wenn *librarylocationtype* beispielsweise cpgenreid ist, gibt dieser Parameter die ID des Genres an, das in der neuen Ansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="bd4d3-119">Diese Zeichenfolge kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="bd4d3-120"> Parameter \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd4d3-121">**Zeichenfolge** , die Parameter enthält, die von Windows Media Player an das Plug-in des Online Stores durch Aufrufen von [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="bd4d3-122">Diese Parameter werden von Windows Media Player nicht interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="bd4d3-123">Sie werden vom Online Shop erstellt und sind nur für den Online Shop von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="bd4d3-124">Diese Zeichenfolge kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="bd4d3-125">*FriendlyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd4d3-126">Eine **Zeichenfolge** , die einen anzeigen Amen enthält, der von Windows Media Player für die dynamische Liste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="bd4d3-127">*ListType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd4d3-128">Eine Bibliotheks Speicherort Konstante, die den Typ der Elemente in der dynamisch generierten Liste angibt.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="bd4d3-129">Wenn der Wert dieses Parameters z. b. cptrackid ist, enthält die dynamische Liste die Spuren.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="bd4d3-130">*ViewMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd4d3-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd4d3-131">Eine **Zeichenfolge** , die den Modus angibt, der von Windows Media Player verwendet wird, um die dynamische Liste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="bd4d3-132">Der Aufrufer muss diesen Parameter auf einen der folgenden Werte festlegen, die in "Contentpartner. h" definiert sind:</span><span class="sxs-lookup"><span data-stu-id="bd4d3-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="bd4d3-133">Viewmodereport</span><span class="sxs-lookup"><span data-stu-id="bd4d3-133">ViewModeReport</span></span>

<span data-ttu-id="bd4d3-134">Viewmodedetails</span><span class="sxs-lookup"><span data-stu-id="bd4d3-134">ViewModeDetails</span></span>

<span data-ttu-id="bd4d3-135">Viewmodeicon</span><span class="sxs-lookup"><span data-stu-id="bd4d3-135">ViewModeIcon</span></span>

<span data-ttu-id="bd4d3-136">Viewmodetile</span><span class="sxs-lookup"><span data-stu-id="bd4d3-136">ViewModeTile</span></span>

<span data-ttu-id="bd4d3-137">Viewmodeorderedlist</span><span class="sxs-lookup"><span data-stu-id="bd4d3-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd4d3-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd4d3-138">Return value</span></span>

<span data-ttu-id="bd4d3-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd4d3-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd4d3-140">Remarks</span></span>

<span data-ttu-id="bd4d3-141">Wenn das Skript auf einer Ermittlungs Seite **changeviewonlinelist** aufruft, übergibt Windows Media Player einige Parameter an die [iwmpcontentpartner:: getlistcontent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) -Methode und die [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) -Methode, die vom Plug-in des Online Stores implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="bd4d3-142">In der folgenden Tabelle wird die Entsprechung zwischen den Parametern der drei Methoden gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="bd4d3-143">changeviewonlinelist-Parameter</span><span class="sxs-lookup"><span data-stu-id="bd4d3-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="bd4d3-144">Getlistcontents-Parameter</span><span class="sxs-lookup"><span data-stu-id="bd4d3-144">GetListContents parameter</span></span> | <span data-ttu-id="bd4d3-145">GetTemplate-Parameter</span><span class="sxs-lookup"><span data-stu-id="bd4d3-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="bd4d3-146">*LocationType*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-146">*LocationType*</span></span>                 | <span data-ttu-id="bd4d3-147">*location*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-147">*location*</span></span>                | <span data-ttu-id="bd4d3-148">*location*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-148">*location*</span></span>            |
| <span data-ttu-id="bd4d3-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-149">*LocationID*</span></span>                   | <span data-ttu-id="bd4d3-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-150">*pContext*</span></span>                | <span data-ttu-id="bd4d3-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-151">*pContext*</span></span>            |
| <span data-ttu-id="bd4d3-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-152">*Params*</span></span>                       | <span data-ttu-id="bd4d3-153">*bstrinbiams*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-153">*bstrParams*</span></span>              | <span data-ttu-id="bd4d3-154">*bstrinviewparametriams*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="bd4d3-155">*Listentyp*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-155">*ListType*</span></span>                     | <span data-ttu-id="bd4d3-156">*bstrinlisttype*</span><span class="sxs-lookup"><span data-stu-id="bd4d3-156">*bstrListType*</span></span>            | <span data-ttu-id="bd4d3-157">nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="bd4d3-157">not applicable</span></span>        |



 

<span data-ttu-id="bd4d3-158">Da alle drei Methoden in der obigen Tabelle durch den Online Shop implementiert werden, haben Sie bei der Verwendung der Parameter eine gewisse Flexibilität.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="bd4d3-159">Die Idee ist, dass Sie genügend Informationen für " **getlistcontent** " bereitstellen, um zu bestimmen, welche Liste abgerufen werden soll, und für " **GetTemplate** " zu ermitteln, welche Ermittlungs Seite als nächstes angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="bd4d3-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="bd4d3-160">In den folgenden Beispielen werden zwei Möglichkeiten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="bd4d3-161">**Beispiel 1: eine dynamische Liste im Katalog des Online Stores**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="bd4d3-162">Angenommen, Sie möchten, dass das Plug-in den Inhalt der dynamischen Liste mit der ID 6 im Katalog des Online Stores erhält.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="bd4d3-163">Angenommen, "List 6" ist eine Liste der Spuren.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="bd4d3-164">Sie können das Plug-in mit ausreichenden Informationen bereitstellen, indem Sie den folgenden-Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="bd4d3-165">Beachten Sie, dass *der Parameter para* meters leer ist. das Plug-in verfügt über genügend Informationen in den anderen Parametern.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="bd4d3-166">**Beispiel 2: eine dynamische Liste, die nicht im Katalog des Online Stores enthalten ist**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="bd4d3-167">Angenommen, Sie möchten, dass das Plug-in den Inhalt einer dynamischen Liste erhält, die nicht im Katalog des Online Stores enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="bd4d3-168">Vielleicht haben Sie sich entschieden, eine dynamische Liste zu haben, die von einem bestimmten Künstler ausgewählte Lieder enthält.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="bd4d3-169">Angenommen, der Künstler hat eine ID von 2 im Katalog des Online Stores.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="bd4d3-170">Sie können den folgenden-Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="bd4d3-171">Beachten Sie, dass die Parameter *LocationType* und *LocationID* die Liste nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="bd4d3-172">Stattdessen gibt der Parameter *para* meters die Liste an.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="bd4d3-173">Die Parameter *LocationType* und *LocationID* werden an **iwmpcontentpartner:: getlistcontent** übermittelt, in diesem Fall können Sie jedoch von **getlistcontent** ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="bd4d3-174">Die *LocationType* -und *LocationID* -Parameter werden ebenfalls an **iwmpcontentpartner:: GetTemplate** übermittelt, die Sie verwenden können, um zu bestimmen, welche Ermittlungs Seite mit der dynamischen Liste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd4d3-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd4d3-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd4d3-175">Requirements</span></span>



| <span data-ttu-id="bd4d3-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd4d3-176">Requirement</span></span> | <span data-ttu-id="bd4d3-177">Wert</span><span class="sxs-lookup"><span data-stu-id="bd4d3-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd4d3-178">Version</span><span class="sxs-lookup"><span data-stu-id="bd4d3-178">Version</span></span><br/> | <span data-ttu-id="bd4d3-179">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="bd4d3-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="bd4d3-180">DLL</span><span class="sxs-lookup"><span data-stu-id="bd4d3-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="bd4d3-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd4d3-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd4d3-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd4d3-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd4d3-183">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="bd4d3-184">**Iwmpcontentpartner:: getlistcontents**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="bd4d3-185">**Iwmpcontentpartnercallback:: addlistcontents**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="bd4d3-186">**Iwmpcontentpartner:: GetTemplate**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="bd4d3-187">**Speicherort und ausgewähltes Element**</span><span class="sxs-lookup"><span data-stu-id="bd4d3-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





