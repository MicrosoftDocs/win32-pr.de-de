---
description: Wenn das FLAG SP \_ COPY \_ NEWER während eines Dateikopiervorgangs angegeben wird, überprüfen die Setupfunktionen, ob eine vorhandene Kopie der Datei im Zielverzeichnis vorhanden ist.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Dateiversionsvergleiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a017549899aa43340f744b1176e7d14ce17d44d60c52b18cfbed9eae3474e99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683180"
---
# <a name="file-version-comparisons"></a>Dateiversionsvergleiche

Wenn das FLAG SP \_ COPY \_ NEWER während eines Dateikopiervorgangs angegeben wird, überprüfen die Setupfunktionen, ob eine vorhandene Kopie der Datei im Zielverzeichnis vorhanden ist. Wenn eine vorhandene Kopie gefunden wird, vergleichen die Funktionen die Versionen der Ziel- und Quelldatei, um zu bestimmen, welche neuer ist.

Die während der Versionsüberprüfungen verwendeten Dateiversionsinformationen sind die, die in den **Membern dwFileVersionMS** und **dwFileVersionLS** einer [**VS \_ FIXEDFILEINFO-Struktur**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) angegeben sind, die von den Versionsfunktionen verwendet werden. Wenn für eine der Dateien keine Versionsressourcen angegeben sind oder wenn sie über die gleichen Versionsinformationen verfügen, wird die Quelldatei als neuere Datei behandelt.

 

 
