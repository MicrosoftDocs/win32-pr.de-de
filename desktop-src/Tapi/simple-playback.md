---
description: Im folgenden Thema wird beschrieben, wie Sie eine einfache Wiedergabe ausführen.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Einfache Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351569"
---
# <a name="simple-playback"></a><span data-ttu-id="d986c-103">Einfache Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d986c-103">Simple Playback</span></span>

<span data-ttu-id="d986c-104">Im folgenden Thema wird beschrieben, wie Sie eine einfache Wiedergabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="d986c-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="d986c-105">**So führen Sie einfache Wiedergabe aus**</span><span class="sxs-lookup"><span data-stu-id="d986c-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="d986c-106">Wählen Sie das Terminal Dateiwiedergabe auf der Ebene des Aufrufes aus.</span><span class="sxs-lookup"><span data-stu-id="d986c-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="d986c-107">Erstellen Sie das Wiedergabe Terminal für den TAPI-Befehl.</span><span class="sxs-lookup"><span data-stu-id="d986c-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="d986c-108">Legen Sie die Eigenschaften – Dateiname und Typ des Speichers fest.</span><span class="sxs-lookup"><span data-stu-id="d986c-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="d986c-109">Öffnen Sie die [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) -Methode im Terminal der Dateiwiedergabe, um die Wiedergabe von Streams zu starten.</span><span class="sxs-lookup"><span data-stu-id="d986c-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="d986c-110">Der folgende Beispielcode veranschaulicht die einfache Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="d986c-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="d986c-111">Erstellen Sie zunächst das Terminal für die Aufzeichnung mithilfe der [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d986c-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="d986c-112">Dies weist den TSP/MSP an, die Dateiwiedergabe bei diesem-Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d986c-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="d986c-113">TSP/MSP erstellt ein Terminal, das von der Anwendung verwendet werden soll, und gibt es bei Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="d986c-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="d986c-114">Holen Sie sich den [**itmediaplayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) -Schnittstellen Zeiger von der Terminal Schnittstelle, und verwenden Sie ihn, um den Dateinamen für die Wiedergabe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d986c-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="d986c-115">Wenn die Datei einen Audiostream enthält und der-Befehl einen Audiodatenstrom aufzeichnen hat, wird der Audioinhalt in der Datei in diesem Stream wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="d986c-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 



