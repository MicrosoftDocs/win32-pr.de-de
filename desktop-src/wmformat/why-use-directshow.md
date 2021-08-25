---
title: Gründe für die Verwendung von DirectShow
description: Gründe für die Verwendung von DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, Hardware
- Windows Medienformat-SDK, Windows-Treibermodell (WDM)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Hardware
- ASF (Advanced Systems Format), Hardware
- Advanced Systems Format (ASF),Windows Driver Model (WDM)
- ASF (Advanced Systems Format),Windows Driver Model (WDM)
- DirectShow, Informationen
- DirectShow, Hardware
- DirectShow,Windows-Treibermodell (WDM)
- Windows Treibermodell (WDM)
- WDM (Windows-Treibermodell)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5edce48be7a806011ba59ab5a2c5328840a18399f6f7eea65d649d52c62402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839420"
---
# <a name="why-use-directshow"></a>Gründe für die Verwendung von DirectShow

Es gibt zwei Hauptgründe, warum eine Anwendung DirectShow anstelle des Windows Media Format SDK direkt verwenden kann: zur Vereinfachung der DirectShow-Streamingarchitektur und für den Zugriff auf Hardware.

## <a name="convenience"></a>Komfort

Bei der DirectShow-Streamingarchitektur sind nur wenige Methodenaufrufe zum Wiedergeben Windows Medienaudio- oder Windows Media Video-Dateien benötigt. Das Erstellen von Dateien wird ebenfalls vereinfacht. Sie geben einfach ein Profil mithilfe der **IConfigAsfWriter-Schnittstelle** für den Filter an, und DirectShow lädt automatisch die erforderlichen Komponenten zum Rendern oder Schreiben der Streams und stellt die Mechanismen zum Übertragen und Synchronisieren des Mediendatenflusses bereit. DirectShow ist besonders nützlich, wenn Inhalte aus unterschiedlichen Formaten in Windows Medienformat konvertiert werden. Sie können DirectShow-Filterdiagramme erstellen, die eine Vielzahl von Datei- und Komprimierungstypen decodieren, und dann die decodierten Datenströme in den [WM ASF Writer-Filter](wm-asf-writer-filter.md) übertragen. Im Vergleich dazu funktioniert das UncompAVItoWMV-Beispiel in diesem SDK nur mit nicht komprimierten AVI-Dateien. Textstreams und beliebige Datenströme können auch über DirectShow erstellt und/oder gerendert werden. Hierfür müssen Sie jedoch möglicherweise benutzerdefinierte DirectShow-Filter für die Verarbeitung dieser Datenströme erstellen.

## <a name="access-to-hardware"></a>Zugriff auf Hardware

DirectShow ist die einzige Möglichkeit für Anwendungscode, auf hardwarebasierte Geräte Windows Driver Model (WDM) zuzugreifen, z.B. 1394 DV-Kameras, TV-Tuner und USB-Webcams. Wenn Ihre Anwendung Daten direkt von einem WDM-basierten Hardwaregerät erfassen und in Windows Medienformat transcodieren muss und das Windows Media Encoder SDK nicht Ihren Anforderungen entspricht, ist DirectShow die einzige Alternative. DirectShow kann auch verwendet werden, um basierend auf Video für Windows auf Legacygeräte zuzugreifen.

 

 




