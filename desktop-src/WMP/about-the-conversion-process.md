---
title: Informationen zum Konvertierungsprozess
description: Informationen zum Konvertierungsprozess
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, Konvertierungsprozess
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038573"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="06209-107">Informationen zum Konvertierungsprozess</span><span class="sxs-lookup"><span data-stu-id="06209-107">About the Conversion Process</span></span>

<span data-ttu-id="06209-108">Nachdem das Konvertierungs-Plug-in von Windows Media Player instanziiert wurde, wird der Prozess wie folgt fortgesetzt:</span><span class="sxs-lookup"><span data-stu-id="06209-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="06209-109">Der Player ruft [iwmpconvert:: convertfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile)auf.</span><span class="sxs-lookup"><span data-stu-id="06209-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="06209-110">Das Plug-in konvertiert die im *bstrinputfile* -Parameter bereitgestellte Datei in ein ASF-Format.</span><span class="sxs-lookup"><span data-stu-id="06209-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="06209-111">Wenn die Konvertierung aus irgendeinem Grund fehlschlägt, gibt das Plug-in einen entsprechenden Fehlercode zurück, und der Prozess wird beendet.</span><span class="sxs-lookup"><span data-stu-id="06209-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="06209-112">Wenn die Konvertierung erfolgreich ist, platziert das Plug-in die konvertierte Datei in dem Ordner, der im Parameter *bstrodestinationfolder* bereitgestellt wird, und gibt den voll qualifizierten Pfad zur konvertierten Datei über den *pbstroutputfile* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="06209-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="06209-113">Das Plug-in gibt einen Erfolgs Code aus **convertfile** zurück.</span><span class="sxs-lookup"><span data-stu-id="06209-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="06209-114">Der Player kopiert die konvertierte Datei in einen Ordner in der Musik Ordnerhierarchie des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="06209-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="06209-115">Genau, wo der Player die Datei kopiert, hängt vom Inhalt ab.</span><span class="sxs-lookup"><span data-stu-id="06209-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="06209-116">Im Rahmen dieses Prozesses kann der Spieler die Datei umbenennen.</span><span class="sxs-lookup"><span data-stu-id="06209-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="06209-117">Der Player kopiert die ursprüngliche (nicht konvertierte) Datei in einen Ordner in der Musik Ordnerhierarchie des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="06209-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="06209-118">Im Rahmen dieses Prozesses kann der Spieler die Datei umbenennen.</span><span class="sxs-lookup"><span data-stu-id="06209-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="06209-119">Dies ist die Kopie der Datei, die der Player verwendet, wenn der Benutzer den Inhalt des Computers mit einem Gerät synchronisiert, das das ursprüngliche Dateiformat erfordert.</span><span class="sxs-lookup"><span data-stu-id="06209-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="06209-120">Diese Datei wird als *Schattendatei* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="06209-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="06209-121">Der-Player Fügt der Bibliothek Informationen zur konvertierten Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="06209-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="06209-122">Dies schließt das Festlegen des Werts für das **shadowfilepath** -Attribut auf den neuen Speicherort ein, an dem die Schattendatei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="06209-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="06209-123">Wenn Sie mit der konvertierten Datei arbeiten müssen, können Sie die Bibliothek Abfragen, um den Inhalt mithilfe der Attribute **contentdistributor** und **WM/UniqueFileIdentifier** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="06209-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="06209-124">Wenn Sie mit der Schattendatei arbeiten müssen, müssen Sie dennoch das **Medien** Objekt für die konvertierte Datei abrufen und dann das **shadowfilepath** -Attribut Abfragen.</span><span class="sxs-lookup"><span data-stu-id="06209-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="06209-125">Siehe [Hinzufügen von Metadaten zu konvertierten Dateien](adding-metadata-to-converted-files.md).</span><span class="sxs-lookup"><span data-stu-id="06209-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06209-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06209-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06209-127">**Informationen zu Konvertierungs-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="06209-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="06209-128">**Hinzufügen von Metadaten zu konvertierten Dateien**</span><span class="sxs-lookup"><span data-stu-id="06209-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="06209-129">**Lesen von Attributwerten**</span><span class="sxs-lookup"><span data-stu-id="06209-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="06209-130">**Shadowfilepath-Attribut**</span><span class="sxs-lookup"><span data-stu-id="06209-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="06209-131">**WM-/contentverteilungs-Attribut**</span><span class="sxs-lookup"><span data-stu-id="06209-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="06209-132">**WM/UniqueFileIdentifier-Attribut**</span><span class="sxs-lookup"><span data-stu-id="06209-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




