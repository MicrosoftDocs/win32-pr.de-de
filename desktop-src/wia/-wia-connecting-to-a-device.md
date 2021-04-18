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
# <a name="connecting-to-a-device"></a>Herstellen einer Verbindung mit einem Gerät

> [!Note]  
> Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt. Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

Der erste Schritt in einer Anwendung oder einem Skript, das das Windows-Abbild Erfassungs Modell (WIA) verwendet, ist das Erstellen des [**WIA**](-wia-wia.md) -Objekts. Dieses Objekt stellt Methoden zum Abrufen einer Auflistung von [**deviceInfo**](-wia-deviceinfo.md) -Objekten bereit und verbindet diese Objekte mit Geräten. Außerdem bietet es die Möglichkeit, auf WIA-Hardware Ereignisse zu lauschen.

In der folgenden Zeile des Microsoft Visual Basic Scripting Edition-Codes (VBScript) wird das [**WIA**](-wia-wia.md) -Objekt erstellt:


```
objWia = CreateObject("Wia.Script")
```



Verwenden Sie nach dem Erstellen des [**WIA**](-wia-wia.md) -Objekts die [**Create**](-wia-iwia-create.md) -Methode, um eine Verbindung mit einem WIA-Hardware Gerät herzustellen.

Sie können auch die [**Devices**](-wia-iwia-devices.md) -Eigenschaft des [**WIA**](-wia-wia.md) -Objekts verwenden, um eine Auflistung von " [**de viceinfo**](-wia-deviceinfo.md) "-Objekten abzurufen. Auflisten Sie diese Auflistung, und verwenden Sie die [**Create**](-wia-iwiadeviceinfo-create.md) -Methode, um eine Verbindung mit einem Gerät herzustellen.

 

 
