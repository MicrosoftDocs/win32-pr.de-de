---
description: Windows Image Acquisition (WIA) stellt Automatisierungsobjekte für die Verwendung in Skriptsprachen wie Microsoft JScript- und Microsoft Visual Basic Scripting Edition(VBScript)-Entwicklungssoftware sowie high-level-Programmiersprachen wie microsoft Visual Basic-Entwicklungssystem zur Verfügung.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: WIA-Skriptmodell
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b558e84dd4095fd0d5dc3f1f14a7de76d9108c488cf3fc3613e3a09bc4830714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812850"
---
# <a name="wia-scripting-model"></a>WIA-Skriptmodell

Windows Image Acquisition (WIA) stellt Automatisierungsobjekte für die Verwendung in Skriptsprachen wie Microsoft JScript- und Microsoft Visual Basic Scripting Edition(VBScript)-Entwicklungssoftware sowie high-level-Programmiersprachen wie microsoft Visual Basic-Entwicklungssystem zur Verfügung.

> [!Note]  
> Dieses Skriptsystem wurde durch die wia Windows Automation Layer (Image Acquisition) ersetzt. Siehe [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

In der folgenden Tabelle werden WIA-Skriptobjekte und deren Verwendung beschrieben. 

| Object                                | BESCHREIBUNG                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wia**](-wia-wia.md)               | Das WIA-Skriptobjekt der obersten Ebene. Verwenden Sie [**das Wia-Objekt**](-wia-wia.md) zum Aufzählen und Herstellen einer Verbindung mit Geräten sowie zum Behandeln von Hardwaregeräteereignissen.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | Das [**DeviceInfo-Objekt**](-wia-deviceinfo.md) bietet Zugriff auf Informationen zu Geräteeigenschaften.                                                                                     |
| [**Element**](-wia-item.md)             | Dieses Objekt stellt WIA-Geräte-, Datei- und Ordnerelemente dar. Ein WIA-Hardwaregerät und seine Bilder oder Scanbilder werden als hierarchische Struktur von [**Elementobjekten**](-wia-item.md) dargestellt. |



 

Sowohl das [**DeviceInfo-Objekt**](-wia-deviceinfo.md) als auch das [**Item-Objekt**](-wia-item.md) sind Sammlungsobjekten zugeordnet. Informationen zur Verwendung von Auflistungsobjekten finden Sie unter Verwenden von WIA-Auflistungsobjekten.

In den folgenden Themen werden allgemeine Informationen zur Verwendung des WIA-Skriptmodells behandelt:

-   [Syntaxkonventionen](-wia-syntax-conventions.md)
-   [Verwenden von WIA-Auflistungsobjekten](-wia-using-wia-collection-objects.md)
-   [Definitionen von WIA-Eigenschaftskonst konstanten](-wia-wia-property-constant-definitions.md)

 

 
