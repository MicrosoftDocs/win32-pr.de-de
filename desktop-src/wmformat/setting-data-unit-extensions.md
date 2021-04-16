---
title: Festlegen von Dateneinheiten Erweiterungen
description: Festlegen von Dateneinheiten Erweiterungen
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Erweiterungen für Dateneinheiten, festlegen
- Streams, Dateneinheiten Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516664"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="ae20b-107">Festlegen von Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ae20b-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="ae20b-108">Einige Streams sind für die Verwendung von dateneinheits Erweiterungen konfiguriert, um ergänzenden Daten einzelnen Beispielen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ae20b-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="ae20b-109">Weitere Informationen zu erweiterten Beispielen finden Sie unter [Dateneinheiten Erweiterungen](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ae20b-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="ae20b-110">Die meisten Dateneinheiten Erweiterungs Systeme erfordern eine Erweiterung in jedem Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="ae20b-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="ae20b-111">Wenn Sie keine Erweiterung der richtigen Größe angeben, wird das Beispiel vom Writer abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="ae20b-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="ae20b-112">Wenn Sie einem Beispiel erweiterte Daten hinzufügen möchten, verwenden Sie die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ae20b-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="ae20b-113">Informationen zu den für einen Stream konfigurierten Dateneinheiten Erweiterungen finden Sie unter Verwendung der Methoden [**IWMStreamConfig2:: getdataunitextensioncount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) und [**IWMStreamConfig2:: getdataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="ae20b-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae20b-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae20b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae20b-115">**Konfigurieren von Dateneinheitserweiterung en**</span><span class="sxs-lookup"><span data-stu-id="ae20b-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="ae20b-116">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="ae20b-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




