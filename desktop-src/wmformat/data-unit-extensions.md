---
title: Dateneinheiten Erweiterungen
description: Dateneinheiten Erweiterungen
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media-Format-SDK, Dateneinheiten Erweiterungen
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Windows Media-Format-SDK, Nutz Last Erweiterungs Systeme
- Advanced Systems Format (ASF), Nutz Last Erweiterungs Systeme
- ASF (Advanced Systems Format), Nutz Last Erweiterungs Systeme
- Dateneinheiten Erweiterungen, Informationen zu
- Nutz Last Einheiten Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723496"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="3cfc7-111">Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="3cfc7-111">Data Unit Extensions</span></span>

<span data-ttu-id="3cfc7-112">Mit dem Windows Media-Format-SDK können Sie Daten in Beispielen mit *Dateneinheiten Erweiterungen* ergänzen, die auch als Nutz Last Erweiterungs Systeme bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="3cfc7-113">In dieser Dokumentation wird der Begriff "Dateneinheiten Erweiterungen" verwendet, damit Sie mit Methodennamen wie [**adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)konsistent bleiben.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="3cfc7-114">Eine Dateneinheiten Erweiterung ist ein Name-Wert-Paar, das im Daten Abschnitt der Datei an das Beispiel angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="3cfc7-115">Sie können auf die erweiterten Daten mithilfe der Methoden des Buffer-Objekts zugreifen, wenn das Beispiel vom Reader abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="3cfc7-116">Sie können Dateneinheiten Erweiterungen für Ihre eigenen Spezifikationen erstellen, aber mehrere Typen sind vordefiniert und werden von den Objekten dieses SDK unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="3cfc7-117">Diese Standard Erweiterungen werden verwendet, um zusätzliche Daten für Dateinamen (in Skript-und Webstreams), SMPTE-Zeit Code Daten, ein nicht quadratisches Pixel-Seitenverhältnis, eine Dauer und einen Typ von Interlacing bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="3cfc7-118">Um dateneinheits Erweiterungen zu verwenden, müssen Sie den Stream so konfigurieren, dass Sie akzeptiert werden, und dann den einzelnen Beispielen für diesen Stream Erweiterungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3cfc7-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cfc7-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cfc7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cfc7-120">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="3cfc7-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="3cfc7-121">**Konfigurieren von Dateneinheitserweiterung en**</span><span class="sxs-lookup"><span data-stu-id="3cfc7-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="3cfc7-122">**Festlegen von Dateneinheiten Erweiterungen**</span><span class="sxs-lookup"><span data-stu-id="3cfc7-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




