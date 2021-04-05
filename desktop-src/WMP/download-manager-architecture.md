---
title: Architektur des Download-Managers
description: Architektur des Download-Managers
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Architektur für Download-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708561"
---
# <a name="download-manager-architecture"></a>Architektur des Download-Managers

Der Windows Media Player Download-Manager verwendet die com-Technologie. Die Funktionalität wird in einer Reihe von Programmierschnittstellen destilliert. Sie können Programmiercode schreiben, der diese Schnittstellen mithilfe von Microsoft JScript oder C++ verwendet.

Die Skriptsprachen verwenden das Konzept von-Objekten, um Programmierfunktionen zu unterteilen. Das **Download Manager** -Objektmodell verwendet mehrere Objekte, um die Methoden und Eigenschaften in eine logische Organisation aufzuteilen, in der semantisch verwandte Funktionen gruppiert werden. Die folgenden Abschnitte enthalten Informationen zu den Download-Manager-Objekten.



| `Section`                                                                     | BESCHREIBUNG                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Informationen zum Download Manager-Objekt](#about-the-downloadmanager-object)       | Das **Download Manager** -Objekt stellt das Stamm Objekt für den Windows Media Player Download-Manager dar. |
| [Informationen zum downloadcollection-Objekt](#about-the-downloadcollection-object) | Das **downloadcollection** -Objekt stellt eine Auflistung von Download Elementen dar.                             |
| [Informationen zum "Downloader"-Objekt](#about-the-downloaditem-object)             | Das **downloadaditem** -Objekt stellt eine einzelne Download Anforderung dar.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Informationen zum Download Manager-Objekt

**Download Manager** ist das Stamm Objekt für den Windows Media Player Download-Manager. Der Zugriff auf alle anderen Objekte erfolgt über dieses Objekt. Um Zugriff auf das **Download Manager** -Objekt zu erhalten, verwenden Sie die folgende JScript-Syntax:


```C++
var DownloadManager = external.DownloadManager;
```



Dadurch wird eine Instanz des **Downloadmanager** -Objekts erstellt, die dann zum Abrufen der untergeordneten Objekte verwendet werden kann. Mit der folgenden Syntax wird z. b. das erste Element aus der Download Auflistung mit der ID-Nummer 253675 abgerufen:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Informationen zum downloadcollection-Objekt

Das **downloadcollection** -Objekt stellt eine Auflistung der herunter zuladenden Dateien dar. Mit diesem Objekt können Sie feststellen, wie viele Downloads in der Sammlung sind, Elemente aus der Sammlung entfernen, ein bestimmtes Download Element abrufen und einen neuen Download starten. Beim Starten eines neuen Downloads wird der Download automatisch der Sammlung hinzugefügt.

## <a name="about-the-downloaditem-object"></a>Informationen zum "Downloader"-Objekt

Das **downloadaditem** -Objekt stellt einen einzelnen Download dar. Download Elemente sind immer als Teil einer Download Sammlung vorhanden. Verwenden Sie dieses Objekt, um Informationen zum Download Element abzurufen und den aktuell ausgeführten Download anzuhalten, fortzusetzen oder abzubrechen.

Wenn Sie einen Download abbrechen, bleibt das Download Element in der Download Sammlung erhalten. In diesem Fall **downloadcollection**. **DownloadState** Ruft den Wert 4 ab, d. h. abgebrochen.

Sie können " **Downloader**" verwenden. der **Fortschritt** , um den Benutzer darüber zu informieren, welcher Teil der Datei übertragen wurde oder wie viel heruntergeladen werden muss. Sie können diesen Wert auch verwenden, um die verbleibende Zeit zu schätzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Download-Manager**](download-manager.md)
</dt> </dl>

 

 




