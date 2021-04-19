---
title: Download Collection. startDownload-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die startDownload-Methode fügt einen Download zur Warteschlange.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- startDownload-Methode, Windows-Media Player
- startDownload-Methode, Windows Media Player, downloadcollection-Klasse
- Download Collection-Klasse, Windows Media Player, startDownload-Methode
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370273"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="b509c-108">Download Collection. startDownload-Methode</span><span class="sxs-lookup"><span data-stu-id="b509c-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="b509c-109">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="b509c-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b509c-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b509c-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b509c-111">Die **startDownload** -Methode fügt einen Download zur Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="b509c-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="b509c-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="b509c-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="b509c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b509c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b509c-114">*SourceUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b509c-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b509c-115">**Zeichenfolge** , die die URL des Downloads angibt.</span><span class="sxs-lookup"><span data-stu-id="b509c-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="b509c-116">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b509c-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b509c-117">**Zeichenfolge** , die den Typ des Downloads angibt.</span><span class="sxs-lookup"><span data-stu-id="b509c-117">**String** specifying the type of download.</span></span> <span data-ttu-id="b509c-118">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="b509c-118">Contains one of the following values.</span></span>



| <span data-ttu-id="b509c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b509c-119">Value</span></span>      | <span data-ttu-id="b509c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b509c-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b509c-121">background</span><span class="sxs-lookup"><span data-stu-id="b509c-121">background</span></span> | <span data-ttu-id="b509c-122">(Windows XP und höher.) Der Download erfolgt als Hintergrundprozess, wenn die Prozessorzeit verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="b509c-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="b509c-123">Download Zustände bleiben auch dann erhalten, wenn Windows Media Player oder Windows XP heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="b509c-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="b509c-124">Echt Zeit</span><span class="sxs-lookup"><span data-stu-id="b509c-124">real time</span></span>  | <span data-ttu-id="b509c-125">(Alle unterstützten Betriebssysteme) Der Download erfolgt alle auf einmal.</span><span class="sxs-lookup"><span data-stu-id="b509c-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="b509c-126">Zwischen den Sitzungen bleiben keine Download Zustände erhalten.</span><span class="sxs-lookup"><span data-stu-id="b509c-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b509c-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b509c-127">Return value</span></span>

<span data-ttu-id="b509c-128">Diese Methode gibt ein-Objekt vom Typ " **Downloader** " zurück.</span><span class="sxs-lookup"><span data-stu-id="b509c-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b509c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b509c-129">Remarks</span></span>

<span data-ttu-id="b509c-130">Wenn ein neuer Download gestartet wird, fügt der Download-Manager ihn als Element der Download Sammlung hinzu, die den Download initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="b509c-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="b509c-131">Es können nur die folgenden Digital Media-Formate heruntergeladen werden:</span><span class="sxs-lookup"><span data-stu-id="b509c-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="b509c-132">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="b509c-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="b509c-133">MP3</span><span class="sxs-lookup"><span data-stu-id="b509c-133">MP3</span></span>
-   <span data-ttu-id="b509c-134">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="b509c-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="b509c-135">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="b509c-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="b509c-136">Der *SourceUrl* -Parameter unterstützt keine Unicode-codierten Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="b509c-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="b509c-137">Er muss auf gültigen Inhalt zeigen.</span><span class="sxs-lookup"><span data-stu-id="b509c-137">It must point to valid content.</span></span> <span data-ttu-id="b509c-138">Umleitungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b509c-138">Redirects are not supported.</span></span>

<span data-ttu-id="b509c-139">Bei der Verwendung von Windows XP werden Audiodateien automatisch in die entsprechenden **eigenen Musik** -Unterordner auf der Grundlage von Metadatenwerten auf Dateiebene platziert.</span><span class="sxs-lookup"><span data-stu-id="b509c-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="b509c-140">Video Dateien werden in \\ den Zufallszahlen-Typ für den Musik \\ Download eingefügt \\  \\ , wobei " *Random Number* " ein von Windows Media Player für jeden Benutzer generierter zufälliger Wert ist, und " *Type* " ist abhängig vom Downloadtyp entweder "Real Time" oder "Background".</span><span class="sxs-lookup"><span data-stu-id="b509c-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="b509c-141">Bei der Verwendung von Windows Media Player 9-Serie mit Windows 98 und Windows Millennium Edition (Me) werden Audiodateien und Videodateien in \\ den \\ \\ *Zufallszahlen*-Typ "Musikdownload" eingefügt \\ , wobei " *Random Number* " ein zufälliger Wert ist, der vom Player für jeden Benutzer generiert wird, und " *Type* " ist abhängig vom Downloadtyp entweder "Real Time" oder "Background".</span><span class="sxs-lookup"><span data-stu-id="b509c-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="b509c-142">Beachten Sie, dass Dateien möglicherweise auf der Grundlage der in der Datei enthaltenen Metadatenattribute und der vom Benutzer im Dialogfeld **Optionen** angegebenen Regeln umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="b509c-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="b509c-143">Dateien, die keine Metadaten enthalten (z. b. **Album** oder **Artist**), werden möglicherweise in Ordner mit der Bezeichnung Unknown Artist oder Unknown Album verschoben.</span><span class="sxs-lookup"><span data-stu-id="b509c-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="b509c-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b509c-144">Requirements</span></span>



| <span data-ttu-id="b509c-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b509c-145">Requirement</span></span> | <span data-ttu-id="b509c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="b509c-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b509c-147">Version</span><span class="sxs-lookup"><span data-stu-id="b509c-147">Version</span></span><br/> | <span data-ttu-id="b509c-148">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="b509c-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="b509c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b509c-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="b509c-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b509c-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b509c-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b509c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b509c-152">**Download Collection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b509c-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="b509c-153">**Download Item-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b509c-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





