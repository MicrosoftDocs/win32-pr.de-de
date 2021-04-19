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
# <a name="wia-scripting-model"></a>WIA-Skript Modell

Die Windows-Abbild Beschaffung (WIA) stellt Automatisierungs Objekte zur Verwendung in Skriptsprachen bereit, wie z. b. Microsoft JScript und Microsoft Visual Basic Scripting Edition (VBScript)-Entwicklungssoftware, und Programmiersprachen auf allgemeiner Ebene, wie z. b. Microsoft Visual Basic Entwicklungssystem.

> [!Note]  
> Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt. Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

In der folgenden Tabelle werden WIA-Skript Erstellungs Objekte und deren Verwendung beschrieben. 

| Object                                | BESCHREIBUNG                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WIA**](-wia-wia.md)               | Das WIA-Skript Objekt der obersten Ebene. Verwenden Sie das [**WIA**](-wia-wia.md) -Objekt, um Geräte aufzulisten und zu verbinden und um Hardware Geräte Ereignisse zu verarbeiten.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | Das [**deviceInfo**](-wia-deviceinfo.md) -Objekt bietet Zugriff auf Informationen zu den Geräteeigenschaften.                                                                                     |
| [**Element**](-wia-item.md)             | Dieses Objekt stellt WIA-Geräte-, Datei-und Ordner Elemente dar. Ein WIA-Hardware Gerät und seine Images oder scannerbetten werden als hierarchische Struktur von [**Item**](-wia-item.md) -Objekten dargestellt. |



 

Das Objekt " [**de viceinfo**](-wia-deviceinfo.md) " und das [**Item**](-wia-item.md) -Objekt werden Auflistungs Objekten zugeordnet. Weitere Informationen zum Verwenden von Sammlungsobjekten finden Sie unter Verwenden von WIA-Auflistungs Objekten.

In den folgenden Themen werden allgemeine Informationen zur Verwendung des WIA-Skript Modells behandelt:

-   [Syntaxkonventionen](-wia-syntax-conventions.md)
-   [Verwenden von WIA-Sammlungsobjekten](-wia-using-wia-collection-objects.md)
-   [Eigenschafts Konstante Definitionen von WIA](-wia-wia-property-constant-definitions.md)

 

 
