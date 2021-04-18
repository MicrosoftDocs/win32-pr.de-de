---
description: 'Weitere Informationen finden Sie unter: Herstellen einer Verbindung mit einem Gerät'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Herstellen einer Verbindung mit einem Gerät
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351696"
---
# <a name="connecting-to-a-device"></a><span data-ttu-id="94d47-103">Herstellen einer Verbindung mit einem Gerät</span><span class="sxs-lookup"><span data-stu-id="94d47-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="94d47-104">Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="94d47-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="94d47-105">Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)</span><span class="sxs-lookup"><span data-stu-id="94d47-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="94d47-106">Der erste Schritt in einer Anwendung oder einem Skript, das das Windows-Abbild Erfassungs Modell (WIA) verwendet, ist das Erstellen des [**WIA**](-wia-wia.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="94d47-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="94d47-107">Dieses Objekt stellt Methoden zum Abrufen einer Auflistung von [**deviceInfo**](-wia-deviceinfo.md) -Objekten bereit und verbindet diese Objekte mit Geräten.</span><span class="sxs-lookup"><span data-stu-id="94d47-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="94d47-108">Außerdem bietet es die Möglichkeit, auf WIA-Hardware Ereignisse zu lauschen.</span><span class="sxs-lookup"><span data-stu-id="94d47-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="94d47-109">In der folgenden Zeile des Microsoft Visual Basic Scripting Edition-Codes (VBScript) wird das [**WIA**](-wia-wia.md) -Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="94d47-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="94d47-110">Verwenden Sie nach dem Erstellen des [**WIA**](-wia-wia.md) -Objekts die [**Create**](-wia-iwia-create.md) -Methode, um eine Verbindung mit einem WIA-Hardware Gerät herzustellen.</span><span class="sxs-lookup"><span data-stu-id="94d47-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="94d47-111">Sie können auch die [**Devices**](-wia-iwia-devices.md) -Eigenschaft des [**WIA**](-wia-wia.md) -Objekts verwenden, um eine Auflistung von " [**de viceinfo**](-wia-deviceinfo.md) "-Objekten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="94d47-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="94d47-112">Auflisten Sie diese Auflistung, und verwenden Sie die [**Create**](-wia-iwiadeviceinfo-create.md) -Methode, um eine Verbindung mit einem Gerät herzustellen.</span><span class="sxs-lookup"><span data-stu-id="94d47-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 
