---
title: Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)
description: Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media-Format-SDK, Erfassen von Geräten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), Erfassung von Geräten (qasf)
- ASF (Advanced Systems Format), Erfassung von Geräten (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Erfassen von Geräten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339217"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)

Wenn Sie Audiodaten oder Videos direkt in einer ASF-Datei erfassen, sieht das Filter Diagramm in etwa wie das folgende Diagramm aus, abhängig vom Typ des verwendeten Erfassungs Geräts.

![Grafik zur WMV-Erfassung](images/asf-webcam.png)

In der DirectShow-SDK-Dokumentation wird ausführlich beschrieben, wie Aufzeichnungs Diagramme erstellt werden. es gibt jedoch einen wichtigen Punkt beim Erstellen von Erfassungs Diagrammen mit dem WM-ASF-Writer: der WM-ASF-Writer wird nicht ausgeführt, es sei denn, alle seine Pins sind verbunden. Wenn Sie den WM-ASF-Writer mit dem Standardsystem Profil (nicht empfohlen) oder einem beliebigen Profil mit Audio-und Videostreams konfigurieren, wird eine Eingabe-PIN für jeden Stream erstellt, und jeder dieser Pins muss verbunden sein. Wenn Sie z. b. keine Audiodaten erfassen möchten, stellen Sie sicher, dass Sie den Filter mit einem nur-Video-Profil konfigurieren, sodass keine audiopin erstellt wird.

 

 




