---
description: Windows Vista nutzt Datei spezifische Miniaturbilder besser als frühere Versionen von Windows.
title: Miniatur Ansichts Handler
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217685"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="4d028-103">Miniatur Ansichts Handler</span><span class="sxs-lookup"><span data-stu-id="4d028-103">Thumbnail Handlers</span></span>

<span data-ttu-id="4d028-104">Windows Vista nutzt Datei spezifische Miniaturbilder besser als frühere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="4d028-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="4d028-105">Windows Vista verwendet diese in allen Ansichten, in Dialogfeldern und für jeden Dateityp, der Sie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4d028-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="4d028-106">Andere Anwendungen können auch die Miniaturansicht nutzen.</span><span class="sxs-lookup"><span data-stu-id="4d028-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="4d028-107">Die Miniaturansicht wurde ebenfalls geändert.</span><span class="sxs-lookup"><span data-stu-id="4d028-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="4d028-108">Nun ist ein kontinuierliches Spektrum von Benutzer auswählbaren Größen verfügbar, und nicht die diskreten Größen wie Symbole und Miniaturansichten, die in Windows XP bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d028-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="4d028-109">Diese Miniaturansichten werden möglicherweise als Live-Symbole bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4d028-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="4d028-110">Miniaturansichten der 32-Bit-Auflösung und so groß wie 256 x 256 Pixel werden häufig in der Windows Vista-Benutzeroberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="4d028-111">Besitzer des Datei Formats sollten darauf vorbereitet sein, die Miniaturansichten in dieser Größe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4d028-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="4d028-112">Sie sollten außerdem nicht statische Bilder für Ihre Miniaturansichten bereitstellen, die den Inhalt der jeweiligen Datei widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4d028-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="4d028-113">Beispielsweise sollte die Miniaturansicht einer Textdatei eine Miniaturversion des Dokuments, einschließlich des Texts, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4d028-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="4d028-114">Die [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle wurde eingeführt, um das Bereitstellen einer Miniaturansicht zu vereinfachen und einfacher als in der Vergangenheit, wenn stattdessen [**iextractimage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) verwendet worden wäre.</span><span class="sxs-lookup"><span data-stu-id="4d028-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="4d028-115">Beachten Sie, dass vorhandener Code, der **iextractimage** verwendet, weiterhin unter Windows Vista gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4d028-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="4d028-116">**Iextractimage** wird jedoch im **Detail** Bereich nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d028-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="4d028-117">In diesem Thema wird Folgendes erörtert:</span><span class="sxs-lookup"><span data-stu-id="4d028-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="4d028-118">Miniatur Ansichts Prozesse</span><span class="sxs-lookup"><span data-stu-id="4d028-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="4d028-119">Miniatur Ansichts Cache und Größenanpassung</span><span class="sxs-lookup"><span data-stu-id="4d028-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="4d028-120">Miniaturansichten Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="4d028-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="4d028-121">Miniatur Ansichts Zusatzelemente</span><span class="sxs-lookup"><span data-stu-id="4d028-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="4d028-122">Registrieren des Miniatur Ansichts Handlers</span><span class="sxs-lookup"><span data-stu-id="4d028-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="4d028-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d028-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="4d028-124">Miniatur Ansichts Prozesse</span><span class="sxs-lookup"><span data-stu-id="4d028-124">Thumbnail Processes</span></span>

<span data-ttu-id="4d028-125">Handler, einschließlich Miniatur Ansichts Handler, werden standardmäßig in einem separaten Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d028-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="4d028-126">Sie können erzwingen, dass der Handler Prozess seitig ausgeführt wird, indem Sie einen **null** -Wert als Bindungs Kontext in einem Aufrufen von [**IShellItem:: bindtohandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) übergeben, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4d028-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="4d028-127">Sie können auch die Ausführung des Out-of-Process-Vorgangs deaktivieren, indem Sie den Eintrag disableprocessisolations in der Registrierung festlegen, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4d028-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="4d028-128">Der Klassen Bezeichner (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} ist die CLSID für [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="4d028-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="4d028-129">Miniatur Ansichts Cache und Größenanpassung</span><span class="sxs-lookup"><span data-stu-id="4d028-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="4d028-130">Wenn eine Miniaturansicht erforderlich ist, prüft Windows zuerst den Miniatur Ansichts Cache auf das Bild.</span><span class="sxs-lookup"><span data-stu-id="4d028-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="4d028-131">Der Miniatur Ansichts Extraktor wird aufgerufen, wenn das Bild nicht im Cache gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="4d028-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="4d028-132">Sie wird auch aufgerufen, wenn der Zeitpunkt der letzten Änderung des Bilds später ist als der der Kopie im Cache.</span><span class="sxs-lookup"><span data-stu-id="4d028-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="4d028-133">Die Miniaturbilder in diesem Cache werden in einem Satz diskreter Größen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4d028-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="4d028-134">Alle Größen werden in Pixel angegeben.</span><span class="sxs-lookup"><span data-stu-id="4d028-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="4d028-135">32 x 32</span><span class="sxs-lookup"><span data-stu-id="4d028-135">32x32</span></span>
-   <span data-ttu-id="4d028-136">96 x 96</span><span class="sxs-lookup"><span data-stu-id="4d028-136">96x96</span></span>
-   <span data-ttu-id="4d028-137">256x256</span><span class="sxs-lookup"><span data-stu-id="4d028-137">256x256</span></span>
-   <span data-ttu-id="4d028-138">1024 x 1024</span><span class="sxs-lookup"><span data-stu-id="4d028-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="4d028-139">Diese Werte können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4d028-139">These values are subject to change.</span></span> <span data-ttu-id="4d028-140">Sie sollten nicht davon ausgehen, dass eine bestimmte Größe immer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d028-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="4d028-141">Wenn ein Bild nicht quadratisch ist, sollten Sie es nicht selbst auffüllen.</span><span class="sxs-lookup"><span data-stu-id="4d028-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="4d028-142">Windows ist dafür verantwortlich, das ursprüngliche Seitenverhältnis zu berücksichtigen und das Bild auf eine quadratische Größe aufzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4d028-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="4d028-143">Wenn ein Image einer bestimmten Größe angefordert wird, ruft Windows Vista immer das nächste größte Bild ab und skaliert es auf die angeforderte Größe, sofern keine genaue Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="4d028-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="4d028-144">Ein Bild wird nie in der Größe zentral hochskaliert, wie es in früheren Versionen von Windows der Fall war.</span><span class="sxs-lookup"><span data-stu-id="4d028-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="4d028-145">In der folgenden Tabelle sind einige Beispiele für die Beziehung zwischen angeforderter Größe und verfügbarer Größe angegeben.</span><span class="sxs-lookup"><span data-stu-id="4d028-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="4d028-146">Maximale Image Größe, die Sie bereitstellen</span><span class="sxs-lookup"><span data-stu-id="4d028-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="4d028-147">Vom Extraktor angeforderte Größe</span><span class="sxs-lookup"><span data-stu-id="4d028-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="4d028-148">Sie stellen</span><span class="sxs-lookup"><span data-stu-id="4d028-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="4d028-149">156 x 120</span><span class="sxs-lookup"><span data-stu-id="4d028-149">156x120</span></span>                        | <span data-ttu-id="4d028-150">256x256</span><span class="sxs-lookup"><span data-stu-id="4d028-150">256x256</span></span>                         | <span data-ttu-id="4d028-151">156x120 (nicht auffüllen, Seitenverhältnis beibehalten)</span><span class="sxs-lookup"><span data-stu-id="4d028-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="4d028-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="4d028-152">2048x1024</span></span>                      | <span data-ttu-id="4d028-153">256x256</span><span class="sxs-lookup"><span data-stu-id="4d028-153">256x256</span></span>                         | <span data-ttu-id="4d028-154">Größe 256x128 (nicht auffüllen, Seitenverhältnis beibehalten)</span><span class="sxs-lookup"><span data-stu-id="4d028-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="4d028-155">Sie können einen Umstellungs Punkt als Teil des Programm-ID-Eintrags der zugeordneten app in der Registrierung deklarieren.</span><span class="sxs-lookup"><span data-stu-id="4d028-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="4d028-156">Unter dieser Größe werden keine Miniaturansichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="4d028-157">Der thumbnailcuumff-Eintrag ist einer dieser reg \_ DWORD-Werte.</span><span class="sxs-lookup"><span data-stu-id="4d028-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="4d028-158">Wert</span><span class="sxs-lookup"><span data-stu-id="4d028-158">Value</span></span> | <span data-ttu-id="4d028-159">Umstellungs</span><span class="sxs-lookup"><span data-stu-id="4d028-159">Cutoff</span></span> | <span data-ttu-id="4d028-160">Hohe dpi-Zeichen</span><span class="sxs-lookup"><span data-stu-id="4d028-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="4d028-161">0</span><span class="sxs-lookup"><span data-stu-id="4d028-161">0</span></span>     | <span data-ttu-id="4d028-162">32 x 32</span><span class="sxs-lookup"><span data-stu-id="4d028-162">32x32</span></span>  | <span data-ttu-id="4d028-163">Ja</span><span class="sxs-lookup"><span data-stu-id="4d028-163">Yes</span></span>               |
| <span data-ttu-id="4d028-164">1</span><span class="sxs-lookup"><span data-stu-id="4d028-164">1</span></span>     | <span data-ttu-id="4d028-165">16 x 16</span><span class="sxs-lookup"><span data-stu-id="4d028-165">16x16</span></span>  | <span data-ttu-id="4d028-166">Ja</span><span class="sxs-lookup"><span data-stu-id="4d028-166">Yes</span></span>               |
| <span data-ttu-id="4d028-167">2</span><span class="sxs-lookup"><span data-stu-id="4d028-167">2</span></span>     | <span data-ttu-id="4d028-168">48x48</span><span class="sxs-lookup"><span data-stu-id="4d028-168">48x48</span></span>  | <span data-ttu-id="4d028-169">Ja</span><span class="sxs-lookup"><span data-stu-id="4d028-169">Yes</span></span>               |
| <span data-ttu-id="4d028-170">3</span><span class="sxs-lookup"><span data-stu-id="4d028-170">3</span></span>     | <span data-ttu-id="4d028-171">16 x 16</span><span class="sxs-lookup"><span data-stu-id="4d028-171">16x16</span></span>  | <span data-ttu-id="4d028-172">Ja</span><span class="sxs-lookup"><span data-stu-id="4d028-172">Yes</span></span>               |


<span data-ttu-id="4d028-173">Die Unterscheidung nach "High dots per inch" (dpi) bedeutet, dass die Pixel Dimensionen der Miniaturansicht automatisch für den größeren dpi-Wert angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="4d028-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="4d028-174">Beispielsweise wäre ein 32 x 32-Bild bei 96 dpi ein 40 x 40-Bild bei 120 dpi.</span><span class="sxs-lookup"><span data-stu-id="4d028-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="4d028-175">Wenn der thumbnailcuumff-Eintrag nicht angegeben wird, ist der Standardwert für "20x20" (nicht dpi-sensibel).</span><span class="sxs-lookup"><span data-stu-id="4d028-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="4d028-176">Miniaturansichten Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="4d028-176">Thumbnail Overlays</span></span>

<span data-ttu-id="4d028-177">Miniaturansichten, ein kleines Bild, das in der unteren rechten Ecke der Miniaturansicht angezeigt wird, bieten Entwicklern die Möglichkeit, Marken Identifizierung auf Ihre Miniaturansichten anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="4d028-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="4d028-178">Überlagerungen werden in der Registrierung als Teil des Programm-ID-Eintrags der zugeordneten App deklariert, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4d028-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="4d028-179">Der typeoverlay-Eintrag enthält einen REG SZ-Wert, der \_ wie folgt interpretiert wird:</span><span class="sxs-lookup"><span data-stu-id="4d028-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="4d028-180">Wenn es sich bei dem Wert um einen Ressourcen Verweis (eine in die DLL eingebettete **ICO** -Datei) wie handelt `ISVComponent.dll,-155` , wird dieses Bild als Überlagerung für Dateien mit dieser Dateinamenerweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="4d028-181">Beachten Sie, dass in diesem Beispiel **155** die Ressourcen-ID ist, und wenn die dll in einem Standardpfad (z. **b. C:/Windows/System32**) nicht vorhanden ist, ist anstelle des DLL-namens der vollständige Pfad erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d028-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="4d028-182">Wenn der Wert eine leere Zeichenfolge ist, wird kein Overlay auf das Bild angewendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="4d028-183">Wenn der Wert nicht vorhanden ist, wird das Standard Symbol der zugeordneten Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="4d028-184">Überlagerungen für Ihre Miniaturansichten sollten nur über diesen Mechanismus bereitgestellt und von Windows angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d028-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="4d028-185">Wenden Sie keine Überlagerungen selbst an.</span><span class="sxs-lookup"><span data-stu-id="4d028-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="4d028-186">Miniatur Ansichts Zusatzelemente</span><span class="sxs-lookup"><span data-stu-id="4d028-186">Thumbnail Adornments</span></span>

<span data-ttu-id="4d028-187">Zusatzelemente, wie z. b. Schlag Schatten, werden auf Miniaturansichten basierend auf dem aktuell ausgewählten Design des Benutzers angewendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="4d028-188">Zusatzelemente werden von Windows bereitgestellt. Erstellen Sie diese nicht selbst.</span><span class="sxs-lookup"><span data-stu-id="4d028-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="4d028-189">Windows könnte das Aussehen bestimmter Zusatzelemente jederzeit ändern. Wenn Sie also eine eigene Ausgabe bereitgestellt haben, würden Sie mit dem System nicht synchron sein.</span><span class="sxs-lookup"><span data-stu-id="4d028-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="4d028-190">Ihre Miniaturansichten können nach unten oder außerhalb des Orts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d028-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="4d028-191">Potenzielle Zusatzelemente werden in der Registrierung als Teil des Programm-ID-Eintrags der zugeordneten App deklariert, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4d028-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="4d028-192">Der Behandlungs Eintrag enthält einen der folgenden reg \_ DWORD-Werte:</span><span class="sxs-lookup"><span data-stu-id="4d028-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="4d028-193">Wert</span><span class="sxs-lookup"><span data-stu-id="4d028-193">Value</span></span> | <span data-ttu-id="4d028-194">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4d028-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="4d028-195">0</span><span class="sxs-lookup"><span data-stu-id="4d028-195">0</span></span>     | <span data-ttu-id="4d028-196">Kein Zusatzelement</span><span class="sxs-lookup"><span data-stu-id="4d028-196">No Adornment</span></span>    |
| <span data-ttu-id="4d028-197">1</span><span class="sxs-lookup"><span data-stu-id="4d028-197">1</span></span>     | <span data-ttu-id="4d028-198">Schatten</span><span class="sxs-lookup"><span data-stu-id="4d028-198">Drop Shadow</span></span>     |
| <span data-ttu-id="4d028-199">2</span><span class="sxs-lookup"><span data-stu-id="4d028-199">2</span></span>     | <span data-ttu-id="4d028-200">Fotorahmen</span><span class="sxs-lookup"><span data-stu-id="4d028-200">Photo Border</span></span>    |
| <span data-ttu-id="4d028-201">3</span><span class="sxs-lookup"><span data-stu-id="4d028-201">3</span></span>     | <span data-ttu-id="4d028-202">Video Sprockets</span><span class="sxs-lookup"><span data-stu-id="4d028-202">Video Sprockets</span></span> |


<span data-ttu-id="4d028-203">Standardmäßig wird ein Schlag Schatten auf Bilder angewendet.</span><span class="sxs-lookup"><span data-stu-id="4d028-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="4d028-204">Registrieren des Miniatur Ansichts Handlers</span><span class="sxs-lookup"><span data-stu-id="4d028-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="4d028-205">Die Registrierung eines Miniatur Ansichts Handlers basiert auf standardmäßigen Dateizuordnungen.</span><span class="sxs-lookup"><span data-stu-id="4d028-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="4d028-206">Die GUID für die Miniatur Ansichts Handler-Shellerweiterung ist `E357FCCD-A995-4576-B01F-234630154E96` .</span><span class="sxs-lookup"><span data-stu-id="4d028-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d028-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d028-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d028-208">**IThumbnailProvider**</span><span class="sxs-lookup"><span data-stu-id="4d028-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="4d028-209">Entwickeln von Miniatur Ansichts Handlern</span><span class="sxs-lookup"><span data-stu-id="4d028-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="4d028-210">Richtlinien für Miniaturansichten</span><span class="sxs-lookup"><span data-stu-id="4d028-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



