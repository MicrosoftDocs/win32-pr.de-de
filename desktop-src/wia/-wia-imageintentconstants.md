---
description: Bild Intent-Konstanten geben an, welche Art von Daten das Image darstellen soll.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Bild Intent Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959091"
---
# <a name="image-intent-constants"></a><span data-ttu-id="f9173-103">Bild Intent-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f9173-103">Image Intent Constants</span></span>

<span data-ttu-id="f9173-104">Bild Intent-Konstanten geben an, welche Art von Daten das Image darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="f9173-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="f9173-105">Die [**\_ \_ cur \_ INTENT**](-wia-wiaitempropscanneritem.md) Scanner-Eigenschaft für WIA-IPS verwendet diese Flags.</span><span class="sxs-lookup"><span data-stu-id="f9173-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="f9173-106">Um eine Absicht bereitzustellen, kombinieren Sie ein beabsichtigtes Abbildtyp Kennzeichen mit einem vorgesehenen size/Quality-Flag, indem Sie den or-Operator verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9173-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="f9173-107">Die WIA- \_ Absicht \_ darf nicht mit anderen Flags kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="f9173-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="f9173-108">Beachten Sie, dass ein Bild nicht gleichzeitig Graustufen und Farben sein darf.</span><span class="sxs-lookup"><span data-stu-id="f9173-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="f9173-109">Im folgenden finden Sie gültige Abbild Intent-Konstanten:</span><span class="sxs-lookup"><span data-stu-id="f9173-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="f9173-110">Vorgesehene Abbildtyp-Flags</span><span class="sxs-lookup"><span data-stu-id="f9173-110">Intended image type flags</span></span>           | <span data-ttu-id="f9173-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9173-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="f9173-112">nicht \_ beabsichtigt \_</span><span class="sxs-lookup"><span data-stu-id="f9173-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="f9173-113">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f9173-113">Default value.</span></span> <span data-ttu-id="f9173-114">Verwenden Sie keine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f9173-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="f9173-115">WIA \_ INTENT \_ Image \_ Type \_ Color</span><span class="sxs-lookup"><span data-stu-id="f9173-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="f9173-116">Vordefinierte Eigenschaften für Farb Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f9173-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="f9173-117">WIA \_ INTENT \_ Image \_ Type \_ Grayscale</span><span class="sxs-lookup"><span data-stu-id="f9173-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="f9173-118">Voreingestellte Eigenschaften für Graustufen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f9173-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="f9173-119">WIA \_ INTENT \_ Image \_ Type \_ Text</span><span class="sxs-lookup"><span data-stu-id="f9173-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="f9173-120">Voreingestellte Eigenschaften für Text Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f9173-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="f9173-121">WIA \_ INTENT \_ Image \_ Type \_ Mask</span><span class="sxs-lookup"><span data-stu-id="f9173-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="f9173-122">Maske für alle Bildtyp-Flags.</span><span class="sxs-lookup"><span data-stu-id="f9173-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="f9173-123">Vorgesehene Image Größe/qualitätsflags</span><span class="sxs-lookup"><span data-stu-id="f9173-123">Intended image size/quality flags</span></span> | <span data-ttu-id="f9173-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9173-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="f9173-125">\_ \_ Minimieren der \_ Größe</span><span class="sxs-lookup"><span data-stu-id="f9173-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="f9173-126">Voreinstellungs Eigenschaften zum Minimieren der Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="f9173-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="f9173-127">WIA- \_ Absicht \_ Maximieren der \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="f9173-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="f9173-128">Voreingestellte Eigenschaften zum Maximieren der Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="f9173-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="f9173-129">WIA \_ INTENT \_ size \_ Mask</span><span class="sxs-lookup"><span data-stu-id="f9173-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="f9173-130">Maske für alle Größen-/qualitätsflags.</span><span class="sxs-lookup"><span data-stu-id="f9173-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="f9173-131">\_ \_ beste \_ Vorschau für WIA</span><span class="sxs-lookup"><span data-stu-id="f9173-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="f9173-132">Gibt die Vorschau der optimalen Qualität an.</span><span class="sxs-lookup"><span data-stu-id="f9173-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="f9173-133">In der folgenden Liste wird der C/C++-Konstantenname gefolgt vom entsprechenden Namen in Klammern angezeigt, der bei der Skripterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9173-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="f9173-134">Die Skriptnamen stammen aus dem wiaintent-enumerierten Typ.</span><span class="sxs-lookup"><span data-stu-id="f9173-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="f9173-135">Beachten Sie, dass nicht alle Konstanten über Skripts verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f9173-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="f9173-136">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="f9173-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="f9173-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9173-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="f9173-138"><dt>**WIA \_ INTENT \_ Image \_ Type \_ Color**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="f9173-139">Vordefinierte Eigenschaften für Farb Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f9173-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="f9173-140"><dt>**WIA \_ INTENT \_ Image \_ Type \_ Grayscale**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="f9173-141">Voreingestellte Eigenschaften für Graustufen Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f9173-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="f9173-142"><dt>**WIA \_ INTENT \_ Image \_ Type \_ Text**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="f9173-143">Voreingestellte Eigenschaften für Text Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f9173-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="f9173-144"><dt>**WIA \_ Beabsichtigte \_ Minimierung der \_ Größe**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="f9173-145">Voreinstellungs Eigenschaften zum Minimieren der Bildgröße.</span><span class="sxs-lookup"><span data-stu-id="f9173-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="f9173-146"><dt>**WIA \_ Absicht \_ Maximieren der \_ Qualität**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="f9173-147">Voreingestellte Eigenschaften zum Maximieren der Bildqualität.</span><span class="sxs-lookup"><span data-stu-id="f9173-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="f9173-148"><dt>**WIA \_ Beabsichtigte \_ beste \_ Vorschau**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="f9173-149">Gibt die Vorschau der optimalen Qualität an.</span><span class="sxs-lookup"><span data-stu-id="f9173-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="f9173-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9173-150">Requirements</span></span>



| <span data-ttu-id="f9173-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9173-151">Requirement</span></span> | <span data-ttu-id="f9173-152">Wert</span><span class="sxs-lookup"><span data-stu-id="f9173-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9173-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9173-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f9173-154">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9173-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f9173-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9173-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f9173-156">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9173-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f9173-157">Header</span><span class="sxs-lookup"><span data-stu-id="f9173-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9173-158"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9173-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




