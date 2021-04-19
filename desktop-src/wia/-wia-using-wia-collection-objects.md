---
description: Eine Auflistung ist ein Objekt, das ein oder mehrere-Objekte enthält. Sammlungen bieten eine effiziente Möglichkeit zum Gruppieren ähnlicher Objekte. Windows-Abbild Beschaffung (WIA) stellt Auflistungen für die Objekte deviceInfo und Item bereit.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Verwenden von WIA-Sammlungsobjekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345118"
---
# <a name="using-wia-collection-objects"></a><span data-ttu-id="b1e7a-105">Verwenden von WIA-Sammlungsobjekten</span><span class="sxs-lookup"><span data-stu-id="b1e7a-105">Using WIA Collection Objects</span></span>

<span data-ttu-id="b1e7a-106">Eine Auflistung ist ein Objekt, das ein oder mehrere-Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="b1e7a-106">A collection is an object that contains one or more objects.</span></span> <span data-ttu-id="b1e7a-107">Sammlungen bieten eine effiziente Möglichkeit zum Gruppieren ähnlicher Objekte.</span><span class="sxs-lookup"><span data-stu-id="b1e7a-107">Collections provide an efficient way of grouping similar objects.</span></span> <span data-ttu-id="b1e7a-108">Windows-Abbild Beschaffung (WIA) stellt Auflistungen für die Objekte [**deviceInfo**](-wia-deviceinfo.md) und [**Item**](-wia-item.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="b1e7a-108">Windows Image Acquisition (WIA) provides collections for the [**DeviceInfo**](-wia-deviceinfo.md) and [**Item**](-wia-item.md) objects.</span></span>

<span data-ttu-id="b1e7a-109">Verwenden Sie Auflistungen, um die Objekte aufzulisten, die Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1e7a-109">Use collections to enumerate the objects they contain.</span></span> <span data-ttu-id="b1e7a-110">Beispielsweise wird im folgenden VBScript-Beispiel eine Auflistung der [**deviceInfo**](-wia-deviceinfo.md) -Objekte von der [**Devices**](-wia-iwia-devices.md) -Methode abgerufen und dann eine **for... Jede** Schleife zum Durchlaufen der Auflistung:</span><span class="sxs-lookup"><span data-stu-id="b1e7a-110">For example, the following VBScript example obtains a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects from the [**Devices**](-wia-iwia-devices.md) method and then uses a **For...Each** loop to iterate through the collection:</span></span>


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> <span data-ttu-id="b1e7a-111">WIA-Auflistungs Objekte sind 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="b1e7a-111">WIA collection objects are 0-based.</span></span>

 

 

 



