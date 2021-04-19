---
description: Die Windows-Abbild Beschaffung (WIA) stellt Automatisierungs Objekte zur Verwendung in Skriptsprachen bereit, wie z. b. Microsoft JScript und Microsoft Visual Basic Scripting Edition (VBScript)-Entwicklungssoftware, und Programmiersprachen auf allgemeiner Ebene, wie z. b. Microsoft Visual Basic Entwicklungssystem.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: WIA-Skript Modell
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348413"
---
# <a name="wia-scripting-model"></a><span data-ttu-id="a4bc6-103">WIA-Skript Modell</span><span class="sxs-lookup"><span data-stu-id="a4bc6-103">WIA Scripting Model</span></span>

<span data-ttu-id="a4bc6-104">Die Windows-Abbild Beschaffung (WIA) stellt Automatisierungs Objekte zur Verwendung in Skriptsprachen bereit, wie z. b. Microsoft JScript und Microsoft Visual Basic Scripting Edition (VBScript)-Entwicklungssoftware, und Programmiersprachen auf allgemeiner Ebene, wie z. b. Microsoft Visual Basic Entwicklungssystem.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="a4bc6-105">Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="a4bc6-106">Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)</span><span class="sxs-lookup"><span data-stu-id="a4bc6-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="a4bc6-107">In der folgenden Tabelle werden WIA-Skript Erstellungs Objekte und deren Verwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="a4bc6-108">Object</span><span class="sxs-lookup"><span data-stu-id="a4bc6-108">Object</span></span>                                | <span data-ttu-id="a4bc6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4bc6-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4bc6-110">**WIA**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="a4bc6-111">Das WIA-Skript Objekt der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="a4bc6-112">Verwenden Sie das [**WIA**](-wia-wia.md) -Objekt, um Geräte aufzulisten und zu verbinden und um Hardware Geräte Ereignisse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="a4bc6-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="a4bc6-114">Das [**deviceInfo**](-wia-deviceinfo.md) -Objekt bietet Zugriff auf Informationen zu den Geräteeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="a4bc6-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="a4bc6-116">Dieses Objekt stellt WIA-Geräte-, Datei-und Ordner Elemente dar.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="a4bc6-117">Ein WIA-Hardware Gerät und seine Images oder scannerbetten werden als hierarchische Struktur von [**Item**](-wia-item.md) -Objekten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="a4bc6-118">Das Objekt " [**de viceinfo**](-wia-deviceinfo.md) " und das [**Item**](-wia-item.md) -Objekt werden Auflistungs Objekten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="a4bc6-119">Weitere Informationen zum Verwenden von Sammlungsobjekten finden Sie unter Verwenden von WIA-Auflistungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="a4bc6-120">In den folgenden Themen werden allgemeine Informationen zur Verwendung des WIA-Skript Modells behandelt:</span><span class="sxs-lookup"><span data-stu-id="a4bc6-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="a4bc6-121">Syntaxkonventionen</span><span class="sxs-lookup"><span data-stu-id="a4bc6-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="a4bc6-122">Verwenden von WIA-Sammlungsobjekten</span><span class="sxs-lookup"><span data-stu-id="a4bc6-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="a4bc6-123">Eigenschafts Konstante Definitionen von WIA</span><span class="sxs-lookup"><span data-stu-id="a4bc6-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
