---
description: 'Anwendungen können die folgenden Funktionen verwenden, um Gerätedaten mit einem Gerätekontext abzurufen: GetDeviceCaps und devicecapabili.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Abrufen von Gerätedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978305"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="1f70c-103">Abrufen von Gerätedaten</span><span class="sxs-lookup"><span data-stu-id="1f70c-103">Retrieving Device Data</span></span>

<span data-ttu-id="1f70c-104">Anwendungen können die folgenden Funktionen verwenden, um Gerätedaten mit einem Gerätekontext abzurufen: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) und [**devicecapabili.**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)</span><span class="sxs-lookup"><span data-stu-id="1f70c-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="1f70c-105">[**Getabvicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) Ruft allgemeine Gerätedaten für die folgenden Geräte ab:</span><span class="sxs-lookup"><span data-stu-id="1f70c-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="1f70c-106">Raster anzeigen</span><span class="sxs-lookup"><span data-stu-id="1f70c-106">Raster displays</span></span>
-   <span data-ttu-id="1f70c-107">Punkt-Matrix-Drucker</span><span class="sxs-lookup"><span data-stu-id="1f70c-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="1f70c-108">Ink-Jet-Drucker</span><span class="sxs-lookup"><span data-stu-id="1f70c-108">Ink-jet printers</span></span>
-   <span data-ttu-id="1f70c-109">Laser Drucker</span><span class="sxs-lookup"><span data-stu-id="1f70c-109">Laser printers</span></span>
-   <span data-ttu-id="1f70c-110">Vektor Plottern</span><span class="sxs-lookup"><span data-stu-id="1f70c-110">Vector plotters</span></span>
-   <span data-ttu-id="1f70c-111">Raster Kameras</span><span class="sxs-lookup"><span data-stu-id="1f70c-111">Raster cameras</span></span>

<span data-ttu-id="1f70c-112">Die Daten umfassen die unterstützten Funktionen des Geräts, einschließlich der Geräte Auflösung (für Video-anzeigen), des Farb Formats (bei Video-und Farbdruckern), der Anzahl von Grafikobjekten, Raster Funktionen, Kurven Zeichnung, Zeilen Zeichnung, Polygon Zeichnung und Text Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="1f70c-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="1f70c-113">Eine Anwendung ruft diese Daten ab, indem Sie ein Handle bereitstellt, das den entsprechenden Gerätekontext identifiziert, sowie einen Index, der den Typ der Daten angibt, die von der Funktion abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f70c-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="1f70c-114">Die Funktion [**devicecapabiliruft**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) spezifische Daten für Drucker ab, einschließlich der Anzahl der verfügbaren Papierbehälter, der Duplex Funktionen des Druckers, der vom Drucker unterstützten Auflösungen, der maximalen und der minimalen unterstützten Papiergröße usw.</span><span class="sxs-lookup"><span data-stu-id="1f70c-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="1f70c-115">Eine Anwendung ruft diese Daten durch Bereitstellen von Zeichen folgen ab, die ein Druckergerät und einen Port angeben, sowie einen Index, der den Typ der Daten angibt, die von der Funktion abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f70c-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
