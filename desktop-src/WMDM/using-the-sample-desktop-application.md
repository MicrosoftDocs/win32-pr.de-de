---
title: Verwenden der Beispiel-Desktop Anwendung
description: Verwenden der Beispiel-Desktop Anwendung
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- Beispiele, Desktop Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708747"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="79cc0-109">Verwenden der Beispiel-Desktop Anwendung</span><span class="sxs-lookup"><span data-stu-id="79cc0-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="79cc0-110">Bei der Beispiel-Desktop Anwendung handelt es sich um ein grundlegendes Fenster mit zwei Fenstern, das einem Windows-Explorer ähnelt</span><span class="sxs-lookup"><span data-stu-id="79cc0-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="79cc0-111">Es ermöglicht Ihnen das Durchsuchen des Inhalts eines Geräts, das Verwenden einer Strukturansicht der Ordner im linken Bereich und von Dateien im rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="79cc0-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="79cc0-112">Das Stammverzeichnis jeder Ordnerstruktur wird logisch als anderes Gerät betrachtet, obwohl einige Geräte sich selbst als mehrere Objekte (eines für jeden Stamm Speicher) darstellen könnten.</span><span class="sxs-lookup"><span data-stu-id="79cc0-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="79cc0-113">Um die grundlegenden Eigenschaften eines Ordners oder einer Datei zu lesen, klicken Sie mit der rechten Maustaste auf das Objekt, und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="79cc0-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="79cc0-114">Sie können Dateien auf dem Gerät löschen, indem Sie im rechten Bereich eine Datei auswählen und im Menü **Datei** die Option **Löschen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="79cc0-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="79cc0-115">Zum Hinzufügen von Mediendateien zum Gerät können Sie Dateien vom Desktop auf den rechten Bereich des Programms ziehen.</span><span class="sxs-lookup"><span data-stu-id="79cc0-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="79cc0-116">Beachten Sie, dass Dateien ein vom Gerät unterstütztes Medienformat aufweisen müssen. Dateien mit unzulässigen Formaten (nicht-Mediendateien, z. b. txt-Dateien oder Medienformate, die nicht vom Gerät unterstützt werden) werden nicht an das Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="79cc0-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="79cc0-117">(Beachten Sie, dass es sich bei dieser Einschränkung um das Programm handelt. Mithilfe von Windows Media Device Manager können Sie jede beliebige Datei an ein Gerät senden, wenn Sie vom Gerät akzeptiert wird.)</span><span class="sxs-lookup"><span data-stu-id="79cc0-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="79cc0-118">Wenn Sie Rückruf Ereignisse erfassen möchten, die an die [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) -Schnittstelle gesendet werden, müssen Sie die Option "Use Operation Interface" im Menü **Optionen** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="79cc0-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="79cc0-119">Mit dem Menü **Optionen** können Sie auch auswählen, ob Sie mehrere erweiterte Schnittstellen mit Funktionen verwenden möchten, die von erweiterten Geräten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="79cc0-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="79cc0-120">Das Menü **Container** enthält Optionen, mit denen Sie eine Wiedergabeliste oder ein Album erstellen können.</span><span class="sxs-lookup"><span data-stu-id="79cc0-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="79cc0-121">Um eine Wiedergabeliste zu erstellen, wählen Sie mindestens ein Titel auf dem Gerät aus, und klicken Sie im Menü **Container** auf **Wiedergabeliste erstellen** .</span><span class="sxs-lookup"><span data-stu-id="79cc0-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="79cc0-122">Diese Funktion funktioniert nur auf MTP-Geräten, da der Code nur die Erstellung einer "virtuellen" Wiedergabelisten Datei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79cc0-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="79cc0-123">(Eine virtuelle Wiedergabeliste ist eine Wiedergabeliste, die nur durch Metadatenwerte angegeben wird, und nicht durch eine physische Datei (z. b. eine WPL-Datei). Das Gerät muss leere Wiedergabelisten unterstützen, um dieses Feature verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="79cc0-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="79cc0-124">Wenn Sie ein Album (eine Wiedergabeliste mit zugeordneter Grafik) erstellen möchten, wählen Sie ein oder mehrere Titel auf dem Gerät aus, und klicken Sie im Menü **Container** auf **Album erstellen** .</span><span class="sxs-lookup"><span data-stu-id="79cc0-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="79cc0-125">Mit einem Dialogfeld können Sie eine Bilddatei auf Ihrem Computer suchen, die dem Album zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="79cc0-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="79cc0-126">Ähnlich wie bei der Erstellung von Wiedergabelisten erstellt die Anwendung eine "leere" Album Datei. Wenn das Gerät keine leeren Alben unterstützt, funktioniert diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="79cc0-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79cc0-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79cc0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79cc0-128">**Beispiel für eine Desktop Anwendung**</span><span class="sxs-lookup"><span data-stu-id="79cc0-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




