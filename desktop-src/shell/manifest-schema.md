---
description: Diese Elemente bilden das XML-Schema, das im Webpublishing-und Online-Assistenten für das Drucken von Druck Reihen verwendet wird.
title: Schema des Übertragungs Manifests
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994942"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="1bfb7-103">Schema des Übertragungs Manifests</span><span class="sxs-lookup"><span data-stu-id="1bfb7-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="1bfb7-104">Diese Elemente bilden das XML-Schema, das im Webpublishing-und Online-Assistenten für das Drucken von Druck Reihen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="1bfb7-105">Die folgenden Elemente sind für das Übertragungs Manifest definiert.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="1bfb7-106">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="1bfb7-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-109">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-110">failurepage</span><span class="sxs-lookup"><span data-stu-id="1bfb7-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-113">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-114">Ort</span><span class="sxs-lookup"><span data-stu-id="1bfb7-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-117">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-118">datei</span><span class="sxs-lookup"><span data-stu-id="1bfb7-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-120">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-121">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-122">FileList</span><span class="sxs-lookup"><span data-stu-id="1bfb7-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-125">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-126">Pfalz</span><span class="sxs-lookup"><span data-stu-id="1bfb7-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-128">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-129">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-130">folderlist</span><span class="sxs-lookup"><span data-stu-id="1bfb7-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-132">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-133">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-134">formdata</span><span class="sxs-lookup"><span data-stu-id="1bfb7-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-135">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-136">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-137">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-138">htmlui</span><span class="sxs-lookup"><span data-stu-id="1bfb7-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-139">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-140">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-141">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-142">ImageProperty</span><span class="sxs-lookup"><span data-stu-id="1bfb7-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-143">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-144">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-145">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-146">metadata</span><span class="sxs-lookup"><span data-stu-id="1bfb7-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-147">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-148">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-149">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-150">netplace</span><span class="sxs-lookup"><span data-stu-id="1bfb7-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-151">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-152">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-153">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-154">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-155">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-156">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-157">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-158">Größe</span><span class="sxs-lookup"><span data-stu-id="1bfb7-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-159">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-160">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-161">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-162">erfolgreicher Dienst</span><span class="sxs-lookup"><span data-stu-id="1bfb7-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-163">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-164">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-165">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-166">Ziel</span><span class="sxs-lookup"><span data-stu-id="1bfb7-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-167">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-168">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-169">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-170">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1bfb7-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-171">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-172">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-173">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1bfb7-174">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-175">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1bfb7-176">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1bfb7-177">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="1bfb7-178">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="1bfb7-178">cancelledpage</span></span>

<span data-ttu-id="1bfb7-179">Gibt die serverseitige HTML-Seite an, die angezeigt werden soll, bevor der Assistent geschlossen wird, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-180">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-181">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-181">Attributes</span></span>



| <span data-ttu-id="1bfb7-182">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-182">Attribute</span></span> | <span data-ttu-id="1bfb7-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-184">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-184">href</span></span>      | <span data-ttu-id="1bfb7-185">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-185">Required.</span></span> <span data-ttu-id="1bfb7-186">Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-187">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-187">Element Information</span></span>



| <span data-ttu-id="1bfb7-188">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-188">Parent Element</span></span>        | <span data-ttu-id="1bfb7-189">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="1bfb7-190">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-191">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="1bfb7-192">failurepage</span><span class="sxs-lookup"><span data-stu-id="1bfb7-192">failurepage</span></span>

<span data-ttu-id="1bfb7-193">Gibt die serverseitige HTML-Seite an, die angezeigt wird, wenn der Upload nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-194">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-195">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-195">Attributes</span></span>



| <span data-ttu-id="1bfb7-196">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-196">Attribute</span></span> | <span data-ttu-id="1bfb7-197">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-198">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-198">href</span></span>      | <span data-ttu-id="1bfb7-199">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-199">Required.</span></span> <span data-ttu-id="1bfb7-200">Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Upload nicht erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-201">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-201">Element Information</span></span>



| <span data-ttu-id="1bfb7-202">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-202">Parent Element</span></span>        | <span data-ttu-id="1bfb7-203">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1bfb7-204">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-205">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-205">None.</span></span> <span data-ttu-id="1bfb7-206">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="1bfb7-207">speichern</span><span class="sxs-lookup"><span data-stu-id="1bfb7-207">favorite</span></span>

<span data-ttu-id="1bfb7-208">Weist den Assistenten an, einen Favoriten Website Eintrag im Menü " **Favoriten** " für die angegebene URL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="1bfb7-209">Wenn dieses Element nicht angegeben ist, wird das [htmlui](#syntax) -Element an seiner Stelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-210">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-211">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-211">Attributes</span></span>



| <span data-ttu-id="1bfb7-212">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-212">Attribute</span></span> | <span data-ttu-id="1bfb7-213">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-214">comment</span><span class="sxs-lookup"><span data-stu-id="1bfb7-214">comment</span></span>   | <span data-ttu-id="1bfb7-215">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-215">Required.</span></span> <span data-ttu-id="1bfb7-216">Der Kommentar, der dem **Favoriten** Eintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="1bfb7-217">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-217">href</span></span>      | <span data-ttu-id="1bfb7-218">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-218">Required.</span></span> <span data-ttu-id="1bfb7-219">Die URL des **Favoriten** Eintrags.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="1bfb7-220">name</span><span class="sxs-lookup"><span data-stu-id="1bfb7-220">name</span></span>      | <span data-ttu-id="1bfb7-221">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-221">Required.</span></span> <span data-ttu-id="1bfb7-222">Der Name für die URL, die im Menü " **Favoriten** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-223">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-223">Element Information</span></span>



| <span data-ttu-id="1bfb7-224">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-224">Parent Element</span></span>        | <span data-ttu-id="1bfb7-225">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1bfb7-226">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-227">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-227">None.</span></span> <span data-ttu-id="1bfb7-228">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="1bfb7-229">file</span><span class="sxs-lookup"><span data-stu-id="1bfb7-229">file</span></span>

<span data-ttu-id="1bfb7-230">Beschreibt eine einzelne Datei, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-230">Describes a single file to be copied.</span></span> <span data-ttu-id="1bfb7-231">Mehrere [Datei](#syntax) Elemente können unter einem einzelnen [FileList](#syntax) -Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-232">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-233">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-233">Attributes</span></span>



| <span data-ttu-id="1bfb7-234">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-234">Attribute</span></span>   | <span data-ttu-id="1bfb7-235">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-236">ContentType</span><span class="sxs-lookup"><span data-stu-id="1bfb7-236">contenttype</span></span> | <span data-ttu-id="1bfb7-237">Optional.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-237">Optional.</span></span> <span data-ttu-id="1bfb7-238">Der MIME-Typ der Datei.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="1bfb7-239">destination</span><span class="sxs-lookup"><span data-stu-id="1bfb7-239">destination</span></span> | <span data-ttu-id="1bfb7-240">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-240">Required.</span></span> <span data-ttu-id="1bfb7-241">Ein empfohlener Pfad für die Datei, nachdem Sie hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="1bfb7-242">Dieser Pfad ist relativ zur Ziel-URL der uploadwebsite.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="1bfb7-243">Der uploadstandort kann diesen Wert nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="1bfb7-244">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="1bfb7-244">extension</span></span>   | <span data-ttu-id="1bfb7-245">Optional.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-245">Optional.</span></span> <span data-ttu-id="1bfb7-246">Die Dateinamenerweiterung der Datei.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="1bfb7-247">id</span><span class="sxs-lookup"><span data-stu-id="1bfb7-247">id</span></span>          | <span data-ttu-id="1bfb7-248">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-248">Required.</span></span> <span data-ttu-id="1bfb7-249">Der numerische Index der Datei.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="1bfb7-250">size</span><span class="sxs-lookup"><span data-stu-id="1bfb7-250">size</span></span>        | <span data-ttu-id="1bfb7-251">Optional.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-251">Optional.</span></span> <span data-ttu-id="1bfb7-252">Die Größe der Datei (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="1bfb7-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="1bfb7-253">source</span><span class="sxs-lookup"><span data-stu-id="1bfb7-253">source</span></span>      | <span data-ttu-id="1bfb7-254">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-254">Required.</span></span> <span data-ttu-id="1bfb7-255">Der vollständige Dateisystempfad für die Datei.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-256">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-256">Element Information</span></span>



| <span data-ttu-id="1bfb7-257">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-257">Parent Element</span></span>      | <span data-ttu-id="1bfb7-258">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="1bfb7-259">FileList</span><span class="sxs-lookup"><span data-stu-id="1bfb7-259">filelist</span></span>](#syntax) | <span data-ttu-id="1bfb7-260">[Metadaten](#syntax), [Post](#syntax), [Größe ändern](#syntax)</span><span class="sxs-lookup"><span data-stu-id="1bfb7-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="1bfb7-261">FileList</span><span class="sxs-lookup"><span data-stu-id="1bfb7-261">filelist</span></span>

<span data-ttu-id="1bfb7-262">Ein Container für-Elemente, die die zu kopierenden Dateien beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="1bfb7-263">Mehrere [FileList](#syntax) -Elemente können unter einem einzelnen [transfermanifest](#syntax) -Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-264">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-265">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-265">Attributes</span></span>



| <span data-ttu-id="1bfb7-266">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-266">Attribute</span></span>   | <span data-ttu-id="1bfb7-267">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="1bfb7-268">Einsatz Ordner</span><span class="sxs-lookup"><span data-stu-id="1bfb7-268">usesfolders</span></span> | <span data-ttu-id="1bfb7-269">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-270">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-270">Element Information</span></span>



| <span data-ttu-id="1bfb7-271">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-271">Parent Element</span></span>              | <span data-ttu-id="1bfb7-272">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="1bfb7-273">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1bfb7-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="1bfb7-274">datei</span><span class="sxs-lookup"><span data-stu-id="1bfb7-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="1bfb7-275">folder</span><span class="sxs-lookup"><span data-stu-id="1bfb7-275">folder</span></span>

<span data-ttu-id="1bfb7-276">Beschreibt einen Ordner, in dem Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="1bfb7-277">Mehrere [Ordner](#syntax) Elemente können unter einem einzelnen [folderlist](#syntax) -Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-278">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-279">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-279">Attributes</span></span>



| <span data-ttu-id="1bfb7-280">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-280">Attribute</span></span>   | <span data-ttu-id="1bfb7-281">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bfb7-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-282">destination</span><span class="sxs-lookup"><span data-stu-id="1bfb7-282">destination</span></span> | <span data-ttu-id="1bfb7-283">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-283">Required.</span></span> <span data-ttu-id="1bfb7-284">Ein empfohlener Pfad für den Ordner, nachdem er hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="1bfb7-285">Dieser Pfad ist relativ zur Ziel-URL der uploadwebsite.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="1bfb7-286">Der uploadstandort kann diesen Wert nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-287">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-287">Element Information</span></span>



| <span data-ttu-id="1bfb7-288">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-288">Parent Element</span></span>        | <span data-ttu-id="1bfb7-289">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="1bfb7-290">folderlist</span><span class="sxs-lookup"><span data-stu-id="1bfb7-290">folderlist</span></span>](#syntax) | <span data-ttu-id="1bfb7-291">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="1bfb7-292">folderlist</span><span class="sxs-lookup"><span data-stu-id="1bfb7-292">folderlist</span></span>

<span data-ttu-id="1bfb7-293">Ein Container für-Elemente, die die zu kopierenden Dateien beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="1bfb7-294">Mehrere [folderlist](#syntax) -Elemente können unter einem einzelnen [transfermanifest](#syntax) -Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-295">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-296">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-296">Attributes</span></span>

<span data-ttu-id="1bfb7-297">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="1bfb7-298">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-298">Element Information</span></span>



| <span data-ttu-id="1bfb7-299">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-299">Parent Element</span></span>              | <span data-ttu-id="1bfb7-300">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="1bfb7-301">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1bfb7-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="1bfb7-302">Pfalz</span><span class="sxs-lookup"><span data-stu-id="1bfb7-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="1bfb7-303">formdata</span><span class="sxs-lookup"><span data-stu-id="1bfb7-303">formdata</span></span>

<span data-ttu-id="1bfb7-304">Beschreibt optionale HTML-codierte Formulardaten, die mit den Dateien übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="1bfb7-305">Dieses Element wird vom-Dienst hinzugefügt, wenn es für das Hochladen der Dateien als mehrteilige Post-Bereitstellung entscheidet.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="1bfb7-306">Die Formulardaten werden sowie Informationen aus dem [Post](#syntax) -Element verwendet, um den Post-Header zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="1bfb7-307">Unter einem einzelnen [UploadInfo](#syntax) -Knoten können mehrere [formdata](#syntax) -Elemente enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-308">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-309">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-309">Attributes</span></span>



| <span data-ttu-id="1bfb7-310">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-310">Attribute</span></span> | <span data-ttu-id="1bfb7-311">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-312">name</span><span class="sxs-lookup"><span data-stu-id="1bfb7-312">name</span></span>      | <span data-ttu-id="1bfb7-313">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-313">Required.</span></span> <span data-ttu-id="1bfb7-314">Definiert den Formulardaten Namen, der diesem Abschnitt des Uploads zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-315">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-315">Element Information</span></span>



| <span data-ttu-id="1bfb7-316">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-316">Parent Element</span></span>        | <span data-ttu-id="1bfb7-317">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="1bfb7-318">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-319">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="1bfb7-320">htmlui</span><span class="sxs-lookup"><span data-stu-id="1bfb7-320">htmlui</span></span>

<span data-ttu-id="1bfb7-321">Die URL der serverseitigen HTML-Seite, die angezeigt wird, wenn der Assistent geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="1bfb7-322">Dieses Element erstellt einen bevorzugten webseiteneintrag im Menü " **Favoriten** ", wenn das [bevorzugte](#syntax) Element fehlt und der Anzeige Name der uploadwebsite angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-323">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-324">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-324">Attributes</span></span>



| <span data-ttu-id="1bfb7-325">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-325">Attribute</span></span> | <span data-ttu-id="1bfb7-326">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-327">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-327">href</span></span>      | <span data-ttu-id="1bfb7-328">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-328">Required.</span></span> <span data-ttu-id="1bfb7-329">Die URL der serverseitigen HTML-Seite, die angezeigt wird, wenn der Assistent geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-330">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-330">Element Information</span></span>



| <span data-ttu-id="1bfb7-331">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-331">Parent Element</span></span>        | <span data-ttu-id="1bfb7-332">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1bfb7-333">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-334">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-334">None.</span></span> <span data-ttu-id="1bfb7-335">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="1bfb7-336">ImageProperty</span><span class="sxs-lookup"><span data-stu-id="1bfb7-336">imageproperty</span></span>

<span data-ttu-id="1bfb7-337">Gibt eine Bild Eigenschaft in Bezug auf die Datei an.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="1bfb7-338">Mehrere [ImageProperty](#syntax) -Elemente können unter einem einzelnen [Metadatenknoten](#syntax) enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-339">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-340">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-340">Attributes</span></span>



| <span data-ttu-id="1bfb7-341">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-341">Attribute</span></span> | <span data-ttu-id="1bfb7-342">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="1bfb7-343">id</span><span class="sxs-lookup"><span data-stu-id="1bfb7-343">id</span></span>        | <span data-ttu-id="1bfb7-344">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-344">Required.</span></span> <span data-ttu-id="1bfb7-345">Die ID der bestimmten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-346">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-346">Element Information</span></span>



| <span data-ttu-id="1bfb7-347">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-347">Parent Element</span></span>      | <span data-ttu-id="1bfb7-348">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="1bfb7-349">metadata</span><span class="sxs-lookup"><span data-stu-id="1bfb7-349">metadata</span></span>](#syntax) | <span data-ttu-id="1bfb7-350">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-350">None.</span></span> <span data-ttu-id="1bfb7-351">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="1bfb7-352">metadata</span><span class="sxs-lookup"><span data-stu-id="1bfb7-352">metadata</span></span>

<span data-ttu-id="1bfb7-353">Ein Container für Elemente und Text, die Metadaten für die jeweilige Datei definieren.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="1bfb7-354">Mehrere [Metadatenelemente](#syntax) können unter einem einzelnen [Datei](#syntax) Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-355">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-356">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-356">Attributes</span></span>

<span data-ttu-id="1bfb7-357">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="1bfb7-358">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-358">Element Information</span></span>



| <span data-ttu-id="1bfb7-359">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-359">Parent Element</span></span>  | <span data-ttu-id="1bfb7-360">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="1bfb7-361">datei</span><span class="sxs-lookup"><span data-stu-id="1bfb7-361">file</span></span>](#syntax) | [<span data-ttu-id="1bfb7-362">ImageProperty</span><span class="sxs-lookup"><span data-stu-id="1bfb7-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="1bfb7-363">netplace</span><span class="sxs-lookup"><span data-stu-id="1bfb7-363">netplace</span></span>

<span data-ttu-id="1bfb7-364">Definiert das Ziel für einen Netzwerk Speicherort, der nach Abschluss des Uploads an den **Netzwerk Orten** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="1bfb7-365">Die Erstellung eines Netzwerk Orts kann durch die [**ipublishingwizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) -Methode verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-366">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-367">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-367">Attributes</span></span>



| <span data-ttu-id="1bfb7-368">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-368">Attribute</span></span> | <span data-ttu-id="1bfb7-369">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-370">comment</span><span class="sxs-lookup"><span data-stu-id="1bfb7-370">comment</span></span>   | <span data-ttu-id="1bfb7-371">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-371">Required.</span></span> <span data-ttu-id="1bfb7-372">Der Kommentar, der für das Netzwerk Platz Symbol angezeigt wird, wenn der Cursor darauf liegt.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="1bfb7-373">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-373">href</span></span>      | <span data-ttu-id="1bfb7-374">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-374">Required.</span></span> <span data-ttu-id="1bfb7-375">Die URL des Netzwerk Orts Eintrags.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="1bfb7-376">name</span><span class="sxs-lookup"><span data-stu-id="1bfb7-376">name</span></span>      | <span data-ttu-id="1bfb7-377">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-377">Required.</span></span> <span data-ttu-id="1bfb7-378">Der Name für das Symbol für den Netzwerk Platz, der im Ordner " **meine Netzwerk Orte** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-379">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-379">Element Information</span></span>



| <span data-ttu-id="1bfb7-380">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-380">Parent Element</span></span>        | <span data-ttu-id="1bfb7-381">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1bfb7-382">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-383">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-383">None.</span></span> <span data-ttu-id="1bfb7-384">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="1bfb7-385">post</span><span class="sxs-lookup"><span data-stu-id="1bfb7-385">post</span></span>

<span data-ttu-id="1bfb7-386">Die URL, zu der die Datei gepostet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-386">URL to which the file should be posted.</span></span> <span data-ttu-id="1bfb7-387">Dieses Element wird vom-Dienst hinzugefügt, wenn die Übertragung als mehrteilige Post-Übermittlung erfolgt und mit [formdata](#syntax)verwendet wird, um den Post-Header zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="1bfb7-388">Wenn der Dienst die Dateiübertragung mithilfe World Wide Web verteilten Erstellungs-und Versionsverwaltung (WebDAV) durchführen möchte, sollte dieses Element nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="1bfb7-389">Mehrere [Post](#syntax) -Elemente können unter einem einzelnen [Datei](#syntax) Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-390">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-391">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-391">Attributes</span></span>



| <span data-ttu-id="1bfb7-392">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-392">Attribute</span></span> | <span data-ttu-id="1bfb7-393">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bfb7-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-394">Dateiname</span><span class="sxs-lookup"><span data-stu-id="1bfb7-394">filename</span></span>  | <span data-ttu-id="1bfb7-395">Optional.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-395">Optional.</span></span> <span data-ttu-id="1bfb7-396">Der Dateiname für die gepostete Datei.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="1bfb7-397">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-397">href</span></span>      | <span data-ttu-id="1bfb7-398">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-398">Required.</span></span> <span data-ttu-id="1bfb7-399">Die URL des Ziel Ordners.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="1bfb7-400">name</span><span class="sxs-lookup"><span data-stu-id="1bfb7-400">name</span></span>      | <span data-ttu-id="1bfb7-401">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-401">Required.</span></span> <span data-ttu-id="1bfb7-402">Definiert den Formulardaten Namen, der diesem Abschnitt des Beitrags zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-403">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-403">Element Information</span></span>



| <span data-ttu-id="1bfb7-404">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-404">Parent Element</span></span>  | <span data-ttu-id="1bfb7-405">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="1bfb7-406">datei</span><span class="sxs-lookup"><span data-stu-id="1bfb7-406">file</span></span>](#syntax) | [<span data-ttu-id="1bfb7-407">formdata</span><span class="sxs-lookup"><span data-stu-id="1bfb7-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="1bfb7-408">resize</span><span class="sxs-lookup"><span data-stu-id="1bfb7-408">resize</span></span>

<span data-ttu-id="1bfb7-409">Definiert die Skalierung und Neukomprimierung einer Bilddatei in das JPEG-Format.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="1bfb7-410">Wenn die Quelldatei bereits im JPEG-Format vorliegt und kleiner oder gleich der angegebenen Breite und Höhe ist, wird Sie nicht skaliert.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="1bfb7-411">Wenn die Quelldatei keine JPEG-Datei ist, wird Sie konvertiert.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="1bfb7-412">Die Skalierung, Neukomprimierung und Konvertierung der Datei kann durch die [**ipublishingwizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) -Methode verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="1bfb7-413">Mehrere Elemente zur [Größenänderung](#syntax) können unter einem einzelnen [Datei](#syntax) Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-414">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-415">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-415">Attributes</span></span>



| <span data-ttu-id="1bfb7-416">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-416">Attribute</span></span> | <span data-ttu-id="1bfb7-417">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-418">verschoben</span><span class="sxs-lookup"><span data-stu-id="1bfb7-418">cx</span></span>        | <span data-ttu-id="1bfb7-419">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-419">Required.</span></span> <span data-ttu-id="1bfb7-420">Die Breite des Bilds nach dem Hochladen in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="1bfb7-421">Wenn dieser Wert 0 ist, wird **CX** aus dem **CY** -Wert berechnet, um relative Dimensionen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="1bfb7-422">cy</span><span class="sxs-lookup"><span data-stu-id="1bfb7-422">cy</span></span>        | <span data-ttu-id="1bfb7-423">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-423">Required.</span></span> <span data-ttu-id="1bfb7-424">Die Höhe des Bilds nach dem Hochladen in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="1bfb7-425">Wenn dieser Wert 0 ist, wird **CY** aus dem **CX** -Wert berechnet, um relative Dimensionen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="1bfb7-426">Qualität</span><span class="sxs-lookup"><span data-stu-id="1bfb7-426">quality</span></span>   | <span data-ttu-id="1bfb7-427">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-427">Required.</span></span> <span data-ttu-id="1bfb7-428">Der Wert der JPEG-Qualität zwischen 0 und 100, wobei 100 die höchste Qualität ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-429">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-429">Element Information</span></span>



| <span data-ttu-id="1bfb7-430">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-430">Parent Element</span></span>  | <span data-ttu-id="1bfb7-431">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="1bfb7-432">datei</span><span class="sxs-lookup"><span data-stu-id="1bfb7-432">file</span></span>](#syntax) | <span data-ttu-id="1bfb7-433">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="1bfb7-434">erfolgreicher Dienst</span><span class="sxs-lookup"><span data-stu-id="1bfb7-434">successpage</span></span>

<span data-ttu-id="1bfb7-435">Gibt die serverseitige HTML-Seite an, die angezeigt wird, wenn der Upload erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-436">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-437">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-437">Attributes</span></span>



| <span data-ttu-id="1bfb7-438">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-438">Attribute</span></span> | <span data-ttu-id="1bfb7-439">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-440">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-440">href</span></span>      | <span data-ttu-id="1bfb7-441">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-441">Required.</span></span> <span data-ttu-id="1bfb7-442">Die URL der serverseitigen HTML-Seite, die angezeigt werden soll, wenn der Upload erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-443">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-443">Element Information</span></span>



| <span data-ttu-id="1bfb7-444">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-444">Parent Element</span></span>        | <span data-ttu-id="1bfb7-445">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1bfb7-446">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-447">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-447">None.</span></span> <span data-ttu-id="1bfb7-448">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="1bfb7-449">target</span><span class="sxs-lookup"><span data-stu-id="1bfb7-449">target</span></span>

<span data-ttu-id="1bfb7-450">Ein Zielordner, der im UNC-Format (Universal Naming Convention) oder als WebDAV-Server angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="1bfb7-451">Der Dienst fügt dieses Ziel hinzu, um einen Zielordner anzugeben, wenn für die Übertragung ein WebDAV-oder Dateisystem Protokoll verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="1bfb7-452">Wenn der Dienst die Dateiübertragung als mehrteiligen Beitrag ausführt, sollte er dieses Element nicht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-453">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-454">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-454">Attributes</span></span>



| <span data-ttu-id="1bfb7-455">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-455">Attribute</span></span> | <span data-ttu-id="1bfb7-456">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-457">href</span><span class="sxs-lookup"><span data-stu-id="1bfb7-457">href</span></span>      | <span data-ttu-id="1bfb7-458">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-458">Required.</span></span> <span data-ttu-id="1bfb7-459">Die URL des Ziel Ordners.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-459">The URL of the destination folder.</span></span> <span data-ttu-id="1bfb7-460">Verwenden Sie das **https://** -Formular für WebDAV oder das **\\ \\ Server \\ Freigabe** Formular für UNC.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-461">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-461">Element Information</span></span>



| <span data-ttu-id="1bfb7-462">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-462">Parent Element</span></span>        | <span data-ttu-id="1bfb7-463">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1bfb7-464">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1bfb7-465">Keine.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-465">None.</span></span> <span data-ttu-id="1bfb7-466">Text ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="1bfb7-467">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1bfb7-467">transfermanifest</span></span>

<span data-ttu-id="1bfb7-468">Der übergeordnete Knoten der Datei des Übertragungs Manifests.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-469">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-470">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-470">Attributes</span></span>

<span data-ttu-id="1bfb7-471">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="1bfb7-472">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-472">Element Information</span></span>



| <span data-ttu-id="1bfb7-473">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-473">Parent Element</span></span> | <span data-ttu-id="1bfb7-474">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-475">Keine</span><span class="sxs-lookup"><span data-stu-id="1bfb7-475">None</span></span>           | <span data-ttu-id="1bfb7-476">[FileList](#syntax), [folderlist](#syntax), [UploadInfo](#syntax)</span><span class="sxs-lookup"><span data-stu-id="1bfb7-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="1bfb7-477">UploadInfo</span><span class="sxs-lookup"><span data-stu-id="1bfb7-477">uploadinfo</span></span>

<span data-ttu-id="1bfb7-478">Ein Container für-Elemente, die Informationen von der in der Transaktion verwendeten uploadwebsite bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="1bfb7-479">Mehrere [UploadInfo](#syntax) -Elemente können unter einem einzelnen [transfermanifest](#syntax) -Knoten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1bfb7-480">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bfb7-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1bfb7-481">Attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-481">Attributes</span></span>



| <span data-ttu-id="1bfb7-482">attribute</span><span class="sxs-lookup"><span data-stu-id="1bfb7-482">Attribute</span></span>    | <span data-ttu-id="1bfb7-483">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bfb7-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1bfb7-484">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1bfb7-484">friendlyname</span></span> | <span data-ttu-id="1bfb7-485">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-485">Required.</span></span> <span data-ttu-id="1bfb7-486">Ein Anzeige Name für die Website, der im Assistenten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfb7-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1bfb7-487">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="1bfb7-487">Element Information</span></span>



| <span data-ttu-id="1bfb7-488">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="1bfb7-488">Parent Element</span></span>              | <span data-ttu-id="1bfb7-489">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1bfb7-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bfb7-490">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1bfb7-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="1bfb7-491">[cancelledpage](#syntax), [failurepage](#syntax), [Favorit](#syntax), [htmlui](#syntax), [netplace](#syntax), [erfolgreicher spage](#syntax), [target](#syntax)</span><span class="sxs-lookup"><span data-stu-id="1bfb7-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 



