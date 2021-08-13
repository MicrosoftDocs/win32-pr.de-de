---
title: Direkte Erfassung von einem Gerät in einer ASF-Datei (QASF)
description: Direkte Erfassung von einem Gerät in einer ASF-Datei (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Medienformat-SDK, Erfassen von Geräten in ASF-Dateien (QASF)
- Windows Medienformat-SDK, DirectShow
- Advanced Systems Format (ASF), Erfassen von Geräten (QASF)
- ASF (Advanced Systems Format), Erfassen von Geräten (QASF)
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,Erfassen von Geräten in ASF-Dateien (QASF)
- Windows Medienformat-SDK, QASF
- Advanced Systems Format (ASF), QASF
- ASF (Advanced Systems Format), QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570e773e39b4c2d76bd95f0a4ac90269be295585ef91e6e50f653b121cbc8d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705089"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Direkte Erfassung von einem Gerät in einer ASF-Datei (QASF)

Wenn Audio- oder Videodaten direkt in einer ASF-Datei erfasst werden, sieht das Filterdiagramm in etwa wie im folgenden Diagramm aus, je nachdem, welche Art von Erfassungsgerät verwendet wird.

![webcam to wmv capture graph](images/asf-webcam.png)

In der Dokumentation zum DirectShow SDK wird ausführlich beschrieben, wie Erfassungsdiagramme erstellt werden, aber es gibt einen wichtigen Punkt, der beim Erstellen von Erfassungsdiagrammen mit dem WM ASF Writer zu beachten ist: Der WM ASF Writer wird nur ausgeführt, wenn alle pins verbunden sind. Wenn Sie WM ASF Writer mit dem Standardsystemprofil (nicht empfohlen) oder einem Profil mit Audio- und Videostreams konfigurieren, wird ein Eingabepin für jeden Stream erstellt, und jeder dieser Pins muss verbunden sein. Wenn Sie z. B. keine Audioaufzeichnung beabsichtigen, müssen Sie den Filter mit einem profilbasierten Video konfigurieren, damit kein Audiopin erstellt wird.

 

 




