---
description: Das Windows-Abbild Erfassungsgerät (WIA) ist als hierarchische Struktur von iwiaitem-Objekten implementiert.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: WIA-Scanner-Geräte in WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751760"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="b8906-103">WIA-Scanner-Geräte in WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="b8906-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="b8906-104">In diesem Thema wird die Überprüfung der Gerätestruktur für Anwendungen erläutert, die den Windows-Abbild Erfassungs Dienst (WIA) 1,0 verwenden (der unter Windows XP oder früher unterstützt wird).</span><span class="sxs-lookup"><span data-stu-id="b8906-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="b8906-105">Informationen zur Gerätestruktur von Windows-Abbild Erfassungs Elementen (WIA) 2,0 (die unter Windows Vista oder höher unterstützt werden) finden Sie unter [Informationen zur IWiaItem2-Element](-wia-about-item-tree.md)Struktur.</span><span class="sxs-lookup"><span data-stu-id="b8906-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="b8906-106">Das Windows-Abbild Erfassungsgerät (WIA) ist als hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekten implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8906-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="b8906-107">Aus dem Stamm Element kann eine Anwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="b8906-107">From the root item an application may:</span></span>

-   <span data-ttu-id="b8906-108">Funktionen für Abfrage Scanner</span><span class="sxs-lookup"><span data-stu-id="b8906-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="b8906-109">Festlegen der Eigenschaften von Scanner-Geräten</span><span class="sxs-lookup"><span data-stu-id="b8906-109">Set scanner device properties</span></span>
-   <span data-ttu-id="b8906-110">Steuern des Dokument Anlegers</span><span class="sxs-lookup"><span data-stu-id="b8906-110">Control the document feeder</span></span>

<span data-ttu-id="b8906-111">Ein WIA-Überprüfungs Gerät unterscheidet sich von einem WIA-Kamera Gerät, da es im Allgemeinen nicht mehrere Abbilder im Arbeitsspeicher speichert.</span><span class="sxs-lookup"><span data-stu-id="b8906-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="b8906-112">Unterhalb des Stamm Elements verfügt ein typisches Scanner-Objekt über ein einzelnes [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt, das die Daten Sammlungs Funktionen des Geräts darstellt, das Scan Element.</span><span class="sxs-lookup"><span data-stu-id="b8906-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="b8906-113">Für dieses Element ist das [**wiaitemtypefile**](-wia-wia-item-type-flags.md) -Flag festgelegt, um anzugeben, dass Datenübertragungen für dieses Element möglich sind.</span><span class="sxs-lookup"><span data-stu-id="b8906-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="b8906-114">Eine Anwendung richtet einen Scan durch Festlegen der Eigenschaften des Überprüfungs Elements ein, führt die Überprüfung durch und überträgt die Daten mithilfe einer Datenübertragungs Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b8906-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="b8906-115">Das folgende Diagramm veranschaulicht die WIA-Implementierung für einen typischen Scanner:</span><span class="sxs-lookup"><span data-stu-id="b8906-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![WIA-Implementierung eines typischen Scanners](images/wiscantr.gif)

<span data-ttu-id="b8906-117">Ein typischer Duplex Scanner wird in WIA durch ein [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b8906-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="b8906-118">Der Zugriff auf Front-und Back-Page-Daten erfolgt sequenziell auf eine Datenübertragung pro Seite.</span><span class="sxs-lookup"><span data-stu-id="b8906-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="b8906-119">Daher ist die Darstellung eines Duplex Scanners mit der Darstellung eines typischen Scanners identisch.</span><span class="sxs-lookup"><span data-stu-id="b8906-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="b8906-120">Ein Folien Scanner, der mehrere Folien in einem einzelnen Scanvorgang scannen können, stellt jedes separate Bild als separates [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="b8906-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="b8906-121">Das folgende Diagramm veranschaulicht die WIA-Darstellung eines Folien Scanners:</span><span class="sxs-lookup"><span data-stu-id="b8906-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![Folien Scanner](images/wislscan.gif)

 

 



