---
title: Extern. changeView-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die changeView-Methode ändert die Ansicht in Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- changeView-Methode (Windows Media Player)
- changeView-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, changeView-Methode
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373596"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="f14d9-108">Extern. changeView-Methode</span><span class="sxs-lookup"><span data-stu-id="f14d9-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="f14d9-109">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="f14d9-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f14d9-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f14d9-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f14d9-111">Die **changeView** -Methode ändert die Ansicht in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f14d9-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14d9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f14d9-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="f14d9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f14d9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14d9-114">*Librarylocationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f14d9-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14d9-115">Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ der neuen Ansicht angibt.</span><span class="sxs-lookup"><span data-stu-id="f14d9-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="f14d9-116">Beispielsweise gibt die Konstante cpgenreid an, dass in der neuen Ansicht ein bestimmtes Genre angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f14d9-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="f14d9-117">*Librarylocationid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f14d9-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14d9-118">**Zeichenfolge** , die die ID des bestimmten Elements enthält, das in der neuen Ansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f14d9-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="f14d9-119">Wenn *librarylocationtype* beispielsweise cpgenreid ist, gibt dieser Parameter die ID des Genres an, das in der neuen Ansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f14d9-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="f14d9-120">Diese Zeichenfolge kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="f14d9-120">This string can be empty.</span></span> <span data-ttu-id="f14d9-121">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f14d9-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f14d9-122">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f14d9-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14d9-123">**Zeichenfolge** , die den Filter für die neue Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="f14d9-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="f14d9-124">Die Ansicht wird so gefiltert, als ob der Benutzer diesen Text im Word-Wheel-Steuerelement des Players eingegeben hätte.</span><span class="sxs-lookup"><span data-stu-id="f14d9-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="f14d9-125">Diese Zeichenfolge kann leer sein.</span><span class="sxs-lookup"><span data-stu-id="f14d9-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="f14d9-126">*Viewparametriams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f14d9-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14d9-127">**Zeichenfolge** , die Parameter enthält, die von Windows Media Player der neuen Ermittlungs Seite zur Verfügung gestellt werden, die in der neuen Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f14d9-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="f14d9-128">Diese Parameter werden von Windows Media Player nicht interpretiert.</span><span class="sxs-lookup"><span data-stu-id="f14d9-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="f14d9-129">Sie werden vom Online Shop erstellt und sind nur für den Online Shop von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f14d9-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f14d9-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f14d9-130">Return value</span></span>

<span data-ttu-id="f14d9-131">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f14d9-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f14d9-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f14d9-132">Remarks</span></span>

<span data-ttu-id="f14d9-133">In einigen Fällen ist es sinnvoll, den *librarylocationid* -Parameter auf die leere Zeichenfolge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f14d9-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="f14d9-134">Wenn Sie z. b. den *librarylocationtype* -Parameter auf allcpalbumids festlegen, stellt die neue Ansicht Alle Alben dar.</span><span class="sxs-lookup"><span data-stu-id="f14d9-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="f14d9-135">Kein einzelnes Album ist der Schwerpunkt der neuen Ansicht, daher ist es nicht erforderlich, eine Album-ID im *librarylocationid* -Parameter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f14d9-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="f14d9-136">Der *viewparameams* -Parameter bietet die Möglichkeit, eine Ermittlungs Seite mit einer anderen Ermittlungs Seite zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f14d9-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="f14d9-137">Wenn das Skript auf einer Ermittlungs Seite **changeView** aufruft, wird die Benutzeroberfläche von Windows Media Player angepasst.</span><span class="sxs-lookup"><span data-stu-id="f14d9-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="f14d9-138">Diese Anpassung bewirkt, dass der Spieler die [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) -Methode des Plug-Ins aufruft, um die URL einer neuen Ermittlungs Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f14d9-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="f14d9-139">Die Zeichenfolge, die die ursprüngliche Ermittlungs Seite in den *viewparameams* -Parameter übergibt, wird nicht an **GetTemplate** übergeben.</span><span class="sxs-lookup"><span data-stu-id="f14d9-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="f14d9-140">Die neue Ermittlungs Seite kann jedoch die *viewparameterzeichenfolge* abrufen, indem [externe. viewparameters](external-viewparameters.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f14d9-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f14d9-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f14d9-141">Requirements</span></span>



| <span data-ttu-id="f14d9-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f14d9-142">Requirement</span></span> | <span data-ttu-id="f14d9-143">Wert</span><span class="sxs-lookup"><span data-stu-id="f14d9-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f14d9-144">Version</span><span class="sxs-lookup"><span data-stu-id="f14d9-144">Version</span></span><br/> | <span data-ttu-id="f14d9-145">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f14d9-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f14d9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f14d9-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="f14d9-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f14d9-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14d9-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f14d9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14d9-149">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="f14d9-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f14d9-150">**Extern. changeviewonlinelist**</span><span class="sxs-lookup"><span data-stu-id="f14d9-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="f14d9-151">**Extern. librarylocationid**</span><span class="sxs-lookup"><span data-stu-id="f14d9-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="f14d9-152">**Extern. librarylocationtype**</span><span class="sxs-lookup"><span data-stu-id="f14d9-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="f14d9-153">**Extern. viewparameters**</span><span class="sxs-lookup"><span data-stu-id="f14d9-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 





