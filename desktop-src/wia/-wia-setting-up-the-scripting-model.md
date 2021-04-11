---
description: Um das WIA-Skript Modell (Windows Image Acquisition) verwenden zu können, müssen Sie die Datei Wiascr.dll auf dem Computer installiert und registriert haben.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Einrichten der Entwicklungsumgebung für das Skript Modell
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214647"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>Einrichten der Entwicklungsumgebung für das Skript Modell

Um das WIA-Skript Modell (Windows Image Acquisition) verwenden zu können, müssen Sie die Datei Wiascr.dll auf dem Computer installiert und registriert haben.

> [!Note]  
> Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt. Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

Kopieren Sie diese Datei aus dem WIA-SDK in das Verzeichnis *% windir%*/System32 (z. b. c: \\ Windows \\ system32). Navigieren Sie in der Befehlszeile zu diesem Verzeichnis, und geben Sie **regsvr32 Wiascr.dll** ein.

Dies gibt die erforderlichen Informationen in der Systemregistrierung ein.

Sie können jetzt das WIA-Skript Modell verwenden.

 

 
