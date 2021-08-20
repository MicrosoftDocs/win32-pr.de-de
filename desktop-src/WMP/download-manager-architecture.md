---
title: Download-Manager-Architektur
description: Download-Manager-Architektur
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player,Download-Manager
- Onlineshops,Download-Manager
- Typ 2 Onlineshops,Download-Manager
- Windows Media Player,Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Architektur für den Download-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae04be86d935f87202abe4b0bf73e833a9da07cf89526b9dcb60de31eb881a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997100"
---
# <a name="download-manager-architecture"></a>Download-Manager-Architektur

Der Windows Media Player Download-Manager verwendet COM-Technologie. Die Funktionalität wird in eine Reihe von Programmierschnittstellen umgesetzt. Sie können Programmiercode schreiben, der diese Schnittstellen verwendet, indem Sie Microsoft JScript oder C++ verwenden.

Die Skriptsprachen verwenden das Konzept von -Objekten, um die Programmierfunktionalität zu unterteilen. Das **DownloadManager-Objektmodell** verwendet mehrere -Objekte, um die Methoden und Eigenschaften in eine logische Organisation zu unterteilen, die semantisch verknüpfte Funktionen zusammenteilt. Die folgenden Abschnitte enthalten Informationen zu den Download-Manager-Objekten.



| `Section`                                                                     | BESCHREIBUNG                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Informationen zum DownloadManager-Objekt](#about-the-downloadmanager-object)       | Das **DownloadManager-Objekt** stellt das Stammobjekt für den Windows Media Player Download-Manager dar. |
| [Informationen zum DownloadCollection-Objekt](#about-the-downloadcollection-object) | Das **DownloadCollection-Objekt** stellt eine Auflistung von Downloadelementen dar.                             |
| [Informationen zum DownloadItem-Objekt](#about-the-downloaditem-object)             | Das **DownloadItem-Objekt** stellt eine einzelne Downloadanforderung dar.                                   |



 

## <a name="about-the-downloadmanager-object"></a>Informationen zum DownloadManager-Objekt

**DownloadManager** ist das Stammobjekt für den Windows Media Player Download-Manager. Auf alle anderen Objekte wird über dieses Objekt zugegriffen. Um Zugriff auf das **DownloadManager-Objekt zu** erhalten, verwenden Sie die folgende JScript Syntax:


```C++
var DownloadManager = external.DownloadManager;
```



Dadurch wird eine Instanz des **DownloadManager-Objekts** erstellt, das dann zum Abrufen der untergeordneten Objekte verwendet werden kann. Die folgende Syntax ruft beispielsweise das erste Element aus der Downloadsammlung ab, das die ID-Nummer 253675:


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>Informationen zum DownloadCollection-Objekt

Das **DownloadCollection-Objekt** stellt eine Auflistung von Dateien dar, die heruntergeladen werden sollen. Sie können dieses Objekt verwenden, um zu bestimmen, wie viele Downloads in der Sammlung enthalten sind, Elemente aus der Sammlung entfernen, ein bestimmtes Downloadelement abrufen und einen neuen Download starten. Beim Starten eines neuen Downloads wird der Download automatisch der Sammlung hinzufügt.

## <a name="about-the-downloaditem-object"></a>Informationen zum DownloadItem-Objekt

Das **DownloadItem-Objekt** stellt einen einzelnen Download dar. Downloadelemente sind immer als Teil einer Downloadsammlung vorhanden. Verwenden Sie dieses Objekt, um Informationen zum Downloadelement abzurufen und den download in Bearbeitung zu halten, fort aufzunehmen oder abzubricht.

Wenn Sie einen Download abbrechen, bleibt das Downloadelement in seiner Downloadsammlung erhalten. Laden Sie in diesem **FallCollection herunter.** **downloadState** ruft den Wert 4 ab, d. h. abgebrochen.

Sie können **downloadItem verwenden.** **Status,** um den Benutzer darüber zu informieren, wie viel der Datei übertragen wurde oder wie viel noch heruntergeladen werden muss. Sie können diesen Wert auch verwenden, um die verbleibende Zeit zu schätzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Download-Manager**](download-manager.md)
</dt> </dl>

 

 




