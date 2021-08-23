---
description: 'Weitere Informationen zu: Herstellen einer Verbindung mit einem Gerät'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Herstellen einer Verbindung mit einem Gerät
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451220"
---
# <a name="connecting-to-a-device"></a>Herstellen einer Verbindung mit einem Gerät

> [!Note]  
> Dieses Skriptsystem wurde durch Windows Image Acquisition (WIA) Automation Layer ersetzt. Weitere Informationen finden Sie [unter Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Der erste Schritt in jeder Anwendung oder jedem Skript, die das WIA-Skriptmodell (Windows Image Acquisition) verwendet, ist das Erstellen des [**Wia-Objekts.**](-wia-wia.md) Dieses Objekt stellt Methoden für bereit, um eine Sammlung von [**DeviceInfo-Objekten**](-wia-deviceinfo.md) abzurufen und diese Objekte mit Geräten zu verbinden. Sie bietet auch die Möglichkeit, auf WIA-Hardwareereignisse zu lauschen.

Mit der folgenden Zeile von Microsoft Visual Basic Scripting Edition -Code (VBScript) wird das [**Wia-Objekt**](-wia-wia.md) erstellt:


```
objWia = CreateObject("Wia.Script")
```



Verwenden Sie nach dem Erstellen des [**Wia-Objekts**](-wia-wia.md) die [**Create-Methode,**](-wia-iwia-create.md) um eine Verbindung mit einem WIA-Hardwaregerät herzustellen.

Sie können auch die [**Devices-Eigenschaft**](-wia-iwia-devices.md) des [**Wia-Objekts**](-wia-wia.md) verwenden, um eine Sammlung von [**DeviceInfo-Objekten**](-wia-deviceinfo.md) abzurufen. Aufzählen Sie diese Auflistung, und verwenden Sie die [**Create-Methode,**](-wia-iwiadeviceinfo-create.md) um eine Verbindung mit einem Gerät herzustellen.

 

 
