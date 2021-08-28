---
description: Eine Auflistung ist ein -Objekt, das mindestens ein -Objekt enthält. Auflistungen bieten eine effiziente Möglichkeit, ähnliche Objekte zu gruppieren. Windows Image Acquisition (WIA) stellt Sammlungen für die Objekte DeviceInfo und Item bereit.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Verwenden von WIA-Auflistungsobjekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 58a4003394bcc163e9013914da6797a504ec16582b8bfac7915d7a49947c18f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813510"
---
# <a name="using-wia-collection-objects"></a>Verwenden von WIA-Auflistungsobjekten

Eine Auflistung ist ein -Objekt, das mindestens ein -Objekt enthält. Auflistungen bieten eine effiziente Möglichkeit, ähnliche Objekte zu gruppieren. Windows Image Acquisition (WIA) stellt Sammlungen für die [**Objekte DeviceInfo**](-wia-deviceinfo.md) und [**Item**](-wia-item.md) bereit.

Verwenden Sie Auflistungen, um die darin enthaltenen Objekte aufzuzählen. Im folgenden VBScript-Beispiel wird beispielsweise eine Sammlung von [**DeviceInfo-Objekten**](-wia-deviceinfo.md) aus der [**Devices-Methode**](-wia-iwia-devices.md) und anschließend ein **For... Jede** Schleife zum Durchlaufen der Auflistung:


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
> WIA-Sammlungsobjekte sind 0-basiert.

 

 

 



