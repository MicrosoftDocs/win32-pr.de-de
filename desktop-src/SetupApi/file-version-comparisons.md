---
description: Wenn \_ \_ während eines Datei Kopiervorgangs das Flag für neuere SP-Kopien angegeben wird, überprüfen die Setup Funktionen eine vorhandene Kopie der Datei im Zielverzeichnis.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Datei Versions Vergleiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9601dcef07afca81a3ffc64148b0c4f2492f935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363294"
---
# <a name="file-version-comparisons"></a>Datei Versions Vergleiche

Wenn \_ \_ während eines Datei Kopiervorgangs das Flag für neuere SP-Kopien angegeben wird, überprüfen die Setup Funktionen eine vorhandene Kopie der Datei im Zielverzeichnis. Wenn eine vorhandene Kopie gefunden wird, vergleichen die Funktionen die Versionen der Ziel-und Quelldatei, um zu bestimmen, welche neuer ist.

Die Datei Versionsinformationen, die bei Versions Prüfungen verwendet werden, sind die, die in den Elementen **dwfileversionms** und **dwfileversionls** einer [**vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur angegeben sind, die von den Versionsfunktionen verwendet werden. Wenn für eine der Dateien keine Versions Ressourcen angegeben sind oder die gleichen Versionsinformationen vorliegen, wird die Quelldatei als neuere Datei behandelt.

 

 
