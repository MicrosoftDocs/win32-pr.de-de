---
description: Eine Anwendung kann eine komprimierte Datei Teil Weise dekomprimieren, indem Sie die lzseek-und lzread-Funktionen verwendet.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lesen aus komprimierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350380"
---
# <a name="reading-from-compressed-files"></a>Lesen aus komprimierten Dateien

Zusätzlich zur Dekomprimierung einer kompletten Datei in einem einzelnen Vorgang kann eine Anwendung eine komprimierte Datei einzeln dekomprimieren, indem Sie die [**lzseek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) -und [**lzread**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) -Funktionen verwendet. Diese Funktionen sind besonders nützlich, wenn es erforderlich ist, Teile großer Dateien zu extrahieren. Beispielsweise kann ein Schriftart Hersteller neben Zeichendaten auch komprimierte Dateien mit Schriftart Metrik enthalten. Um die Informationen in diesen Dateien zu verwenden, muss eine Anwendung die Datei dekomprimieren. die meisten Anwendungen verwenden allerdings nur einen Teil der Datei zu einem bestimmten Zeitpunkt. Um Informationen über Schriftart Metriken zu erhalten, extrahiert die Anwendung Daten aus dem-Header. Zum Abrufen von Informationen aus dem Text würde die Anwendung den Dateizeiger neu positionieren, indem **lzseek** aufgerufen und Zeichendaten durch Aufrufen von **lzread** extrahiert werden.

 

 



