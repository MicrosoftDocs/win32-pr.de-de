---
title: Param-Element (WMP-SDK)
description: Das param-Element definiert einen benutzerdefinierten Parameter, der einer Wiedergabeliste oder einem Element einer Wiedergabeliste zugeordnet ist.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Param-Element, Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373975"
---
# <a name="param-element"></a><span data-ttu-id="8e0c6-104">Param-Element</span><span class="sxs-lookup"><span data-stu-id="8e0c6-104">PARAM Element</span></span>

<span data-ttu-id="8e0c6-105">Das **param** -Element definiert einen benutzerdefinierten Parameter, der einer Wiedergabeliste oder einem Element einer Wiedergabeliste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="8e0c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e0c6-106">Parameters</span></span>

<span data-ttu-id="8e0c6-107">Ein Parameter kann auch mit der Anzeige anstelle eines einzelnen Clips verknüpft werden, indem dieses Element direkt nach dem **ASX** -Tag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="8e0c6-108">Diese Elemente werden durch ihre Namen und einen Indexwert, der mit Null beginnt, referenziert.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="8e0c6-109">Dieses **ASX** -Element ist nur für Windows Media Player Version 6,01 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="8e0c6-110">Die Standardinstallation von Microsoft Internet Explorer 5 umfasst eine kompatible Version von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="8e0c6-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="8e0c6-111">Attributes</span></span>

<span data-ttu-id="8e0c6-112">**NAME**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-112">**NAME**</span></span>

<span data-ttu-id="8e0c6-113">Der Name, mit dem auf den Parameterwert zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-113">Name used to access the parameter value.</span></span> <span data-ttu-id="8e0c6-114">Der Name kann eine beliebige gültige Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-114">The name can be any valid string.</span></span> <span data-ttu-id="8e0c6-115">Die folgenden Zeichen folgen wurden bereits definiert.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="8e0c6-116">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8e0c6-116">String</span></span>                          | <span data-ttu-id="8e0c6-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e0c6-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0c6-118">AllowShuffle</span><span class="sxs-lookup"><span data-stu-id="8e0c6-118">AllowShuffle</span></span>                    | <span data-ttu-id="8e0c6-119">Das **value** -Attribut gibt an, ob die Metadatendatei-Wiedergabeliste der Windows Media Player Shuffle-Funktion das Abspielen der Einträge in zufälliger Reihenfolge ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="8e0c6-120">Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="8e0c6-121">Der Standardwert ist "No".</span><span class="sxs-lookup"><span data-stu-id="8e0c6-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8e0c6-122">CanPause</span><span class="sxs-lookup"><span data-stu-id="8e0c6-122">CanPause</span></span>                        | <span data-ttu-id="8e0c6-123">Das **value** -Attribut gibt an, ob der Benutzer die Wiedergabe anhalten kann.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="8e0c6-124">Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="8e0c6-125">Der Standardwert ist "yes".</span><span class="sxs-lookup"><span data-stu-id="8e0c6-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8e0c6-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="8e0c6-126">CanSeek</span></span>                         | <span data-ttu-id="8e0c6-127">Das **value** -Attribut gibt an, ob der Benutzer die aktuelle Wiedergabe Position mithilfe der Suchleiste, der schnellen Vorwärtsbewegung oder der schnellen Umkehrung ändern kann.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="8e0c6-128">Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="8e0c6-129">Der Standardwert ist "yes".</span><span class="sxs-lookup"><span data-stu-id="8e0c6-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8e0c6-130">Canskipback</span><span class="sxs-lookup"><span data-stu-id="8e0c6-130">CanSkipBack</span></span>                     | <span data-ttu-id="8e0c6-131">Das **value** -Attribut gibt an, ob der Benutzer **durch Klicken auf** zurück zum vorherigen Wiedergabelisten Element springen kann.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="8e0c6-132">Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="8e0c6-133">Der Standardwert ist "yes".</span><span class="sxs-lookup"><span data-stu-id="8e0c6-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8e0c6-134">Canskipforward</span><span class="sxs-lookup"><span data-stu-id="8e0c6-134">CanSkipForward</span></span>                  | <span data-ttu-id="8e0c6-135">Das **value** -Attribut gibt an, ob der Benutzer durch Klicken auf **weiter** auf das nächste Wiedergabelisten Element springen kann.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="8e0c6-136">Das **value** -Attribut kann auf "yes" oder "No" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="8e0c6-137">Der Standardwert ist "yes".</span><span class="sxs-lookup"><span data-stu-id="8e0c6-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8e0c6-138">Cpradioid</span><span class="sxs-lookup"><span data-stu-id="8e0c6-138">CPRadioID</span></span>                       | <span data-ttu-id="8e0c6-139">Das **value** -Attribut gibt die ID eines Radio Feeds an, der von einem Online Store vom Typ 1 bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="8e0c6-140">Das heißt, das **value** -Attribut muss mit dem Radio ID-Feld eines der Radio Feeds im Katalog des Online Stores identisch sein.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="8e0c6-141">Das übergeordnete Element ist das **ASX** -Element.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8e0c6-142">Codierung</span><span class="sxs-lookup"><span data-stu-id="8e0c6-142">Encoding</span></span>                        | <span data-ttu-id="8e0c6-143">Das **value** -Attribut wird auf "UTF-8" festgelegt, um anzugeben, dass es sich bei der Metadatei um eine Unicode-codierte Datei (UTF-8) handelt.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="8e0c6-144">Htmlllink</span><span class="sxs-lookup"><span data-stu-id="8e0c6-144">HtmlFlink</span></span>                       | <span data-ttu-id="8e0c6-145">Das **value** -Attribut ist eine Zeichenfolge, die von einem Onlinespeicher vom Typ 1 bereitgestellt wird</span><span class="sxs-lookup"><span data-stu-id="8e0c6-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="8e0c6-146">Windows Media Player übergibt die Zeichenfolge an die [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) -Methode, die vom Plug-in des Online Stores implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="8e0c6-147">Die **getiteminfo** -Methode gibt die URL der Webseite zurück, die im Fenster " **jetzt Wiedergabe** " des Players angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="8e0c6-148">Die Webseite hat Zugriff auf alle Methoden, die das **externe** Objekt für den Typ 1 speichert.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="8e0c6-149">Eine Liste dieser Methoden finden Sie unter [externes Objekt für den Typ 1 Online Stores](external-object-for-type-1-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="8e0c6-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="8e0c6-150">HtmlView</span><span class="sxs-lookup"><span data-stu-id="8e0c6-150">HTMLView</span></span>                        | <span data-ttu-id="8e0c6-151">Das **value** -Attribut gibt eine URL an, die im Bereich für die wieder **Gabe** des vollmodusplayers für die Dauer der Wiedergabeliste oder den aktuellen Eintrag angezeigt wird, je nachdem, ob es sich beim übergeordneten Element um das **ASX** -Element oder ein **Entry** -Element handelt.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="8e0c6-152">HtmlView wird für das Windows Media Player-Steuerelement nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8e0c6-153">Log:*FieldName* \[ :*Namespace*\]</span><span class="sxs-lookup"><span data-stu-id="8e0c6-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="8e0c6-154">Das **value** -Attribut gibt den Wert an, auf den das angegeben Protokollfeld festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="8e0c6-155">Der:*Namespace* -Teil des **Name** -Attributs ist optional.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8e0c6-156">Vorab Puffer</span><span class="sxs-lookup"><span data-stu-id="8e0c6-156">Prebuffer</span></span>                       | <span data-ttu-id="8e0c6-157">Das **value** -Attribut gibt an, ob der nächste Wiedergabelisten Eintrag mit der Pufferung vor dem Ende des aktuellen Eintrags beginnt, was einen nahtlosen Übergang ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="8e0c6-158">Das **value** -Attribut kann auf "true" oder "false" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8e0c6-159">Showwhilebuffereing</span><span class="sxs-lookup"><span data-stu-id="8e0c6-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="8e0c6-160">Das **value** -Attribut gibt an, ob eine Bilddatei, auf die vom aktuellen **Eintrags** Element verwiesen wird, weiterhin nach der angegebenen Dauer angezeigt wird, während der nächste Wiedergabelisten Eintrag gepuffert wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="8e0c6-161">Das **value** -Attribut kann auf "true" oder "false" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="8e0c6-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-162">**VALUE**</span></span>

<span data-ttu-id="8e0c6-163">Wert, der diesem Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-163">Value associated with this parameter.</span></span> <span data-ttu-id="8e0c6-164">Dabei kann es sich entweder um einen numerischen oder einen Zeichen folgen Wert handeln.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8e0c6-165">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="8e0c6-165">Parent/Child Elements</span></span>



| <span data-ttu-id="8e0c6-166">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="8e0c6-166">Hierarchy</span></span>       | <span data-ttu-id="8e0c6-167">Elemente</span><span class="sxs-lookup"><span data-stu-id="8e0c6-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="8e0c6-168">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e0c6-168">Parent elements</span></span> | <span data-ttu-id="8e0c6-169">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="8e0c6-170">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8e0c6-170">Child elements</span></span>  | <span data-ttu-id="8e0c6-171">Keine</span><span class="sxs-lookup"><span data-stu-id="8e0c6-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="8e0c6-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e0c6-172">Remarks</span></span>

<span data-ttu-id="8e0c6-173">Dieses Element ermöglicht es Benutzern, zusätzliche Informationen zu den einzelnen Clips im **Eintrags** Element zu platzieren, in dem Sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="8e0c6-174">Verwenden Sie zum Abrufen der im Wiedergabelisten **Eintrag** angegebenen Metadateninformationen das *Medium*. **getiteminfo** -Methode.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="8e0c6-175">Das *Medium*. die **getiteminfo** -Methode ruft den Wert des **value** -Attributs ab, wenn der Name des Parameters angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="8e0c6-176">In früheren Versionen von Windows Media Player die im Wiedergabelisten **Eintrag** angegebenen Metadateninformationen mithilfe der **getmediaparameter** -Methode abgerufen werden, wobei der Name des Parameters und eine Indexnummer für den Eintrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="8e0c6-177">Ein Parameter kann auch mit der Anzeige anstelle eines einzelnen Clips verknüpft werden, indem dieses Element direkt nach dem **ASX** -Tag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="8e0c6-178">Diese Elemente werden durch ihre Namen und einen Indexwert, der mit Null beginnt, referenziert.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="8e0c6-179">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-179">**Note**</span></span>

<span data-ttu-id="8e0c6-180">Dieses **ASX** -Element ist nur für Windows Media Player Version 6,01 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="8e0c6-181">Die Standardinstallation von Microsoft Internet Explorer 5 umfasst eine kompatible Version von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="8e0c6-182">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e0c6-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="8e0c6-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e0c6-183">Requirements</span></span>



| <span data-ttu-id="8e0c6-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e0c6-184">Requirement</span></span> | <span data-ttu-id="8e0c6-185">Wert</span><span class="sxs-lookup"><span data-stu-id="8e0c6-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e0c6-186">Version</span><span class="sxs-lookup"><span data-stu-id="8e0c6-186">Version</span></span><br/> | <span data-ttu-id="8e0c6-187">Windows Media Player Version 7,0 oder höher, Windows Media Player 9 oder höher ist für die vordefinierten namens Attribute erforderlich, Windows Media Player 10 oder höher ist für die vordefinierten Namen "CanPause", "CanSeek", "canskipback" und "canskipforward" erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8e0c6-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e0c6-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e0c6-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e0c6-189">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="8e0c6-190">**Protokollieren von Streamdaten**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="8e0c6-191">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8e0c6-192">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="8e0c6-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





