---
description: Vmrplayer-Beispiel
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Vmrplayer-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863399"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="aa049-103">Vmrplayer-Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa049-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="aa049-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa049-104">Description</span></span>

<span data-ttu-id="aa049-105">Dieses Beispiel verwendet den Filter Video Mischungs-Renderer 9 (VMR-9), um ein oder zwei laufende Videos und ein statisches Bild zu Alpha mischen.</span><span class="sxs-lookup"><span data-stu-id="aa049-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="aa049-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="aa049-106">Usage</span></span>

<span data-ttu-id="aa049-107">Um das erste Video zu öffnen, wählen Sie im Menü **Datei** die Option **primären Stream öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="aa049-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="aa049-108">Wenn Sie ein zweites Video öffnen möchten, wählen Sie im Menü **Datei** den Befehl **sekundären Stream öffnen** aus (Sie müssen zuerst den primären Stream öffnen).</span><span class="sxs-lookup"><span data-stu-id="aa049-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="aa049-109">Um das Video wiederzugeben, klicken Sie auf die Schaltfläche wieder **Gabe** .</span><span class="sxs-lookup"><span data-stu-id="aa049-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="aa049-110">Sie können die Position, Größe und Alpha Werte der Videos festlegen, indem Sie im **VMR-Eigenschaften** Menü den **primären** oder den **sekundären Stream** auswählen.</span><span class="sxs-lookup"><span data-stu-id="aa049-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="aa049-111">Wenn Sie ein statisches Bitmap über das Video hinzufügen möchten, wählen Sie im **VMR-Eigenschaften** Menü die Option **static App Image** aus, und klicken Sie auf das Feld **App-Image**</span><span class="sxs-lookup"><span data-stu-id="aa049-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="aa049-112">Sie können das gleiche Dialogfeld verwenden, um die Position, Größe und den Alpha Wert der Bitmap zu steuern.</span><span class="sxs-lookup"><span data-stu-id="aa049-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="aa049-113">Um das gemischte Video Bild zu erfassen, wählen Sie im **VMR-Eigenschaften** Menü die Option **Bitmapbild erfassen** aus.</span><span class="sxs-lookup"><span data-stu-id="aa049-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="aa049-114">Sie können den primären Bildstream auch über die Befehlszeile angeben:</span><span class="sxs-lookup"><span data-stu-id="aa049-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="aa049-115">**Vmrplayer** **/P** *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="aa049-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="aa049-116">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="aa049-116">Downloading the Sample</span></span>

<span data-ttu-id="aa049-117">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa049-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa049-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa049-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa049-119">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa049-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



