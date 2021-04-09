---
description: Normalerweise werden Debuginformationen in einer Symbol Datei gespeichert, getrennt von der ausführbaren Datei.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Symboldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126055"
---
# <a name="symbol-files"></a>Symboldateien

Normalerweise werden Debuginformationen in einer Symbol Datei gespeichert, getrennt von der ausführbaren Datei. Die Implementierung dieser Debuginformationen hat sich im Laufe der Jahre geändert, und in der folgenden Dokumentation finden Sie Anleitungen zu diesen verschiedenen Implementierungen.

## <a name="pdb-files"></a>PDB-Dateien

Alle modernen Versionen der Microsoft-Compiler speichern Debuginformationen zu einer kompilierten ausführbaren Datei in einer separaten *Programm Daten Bank* Datei (. pdb). Diese Datei wird im Allgemeinen als *PDB* bezeichnet. Die Daten werden in einer separaten Datei der ausführbaren Datei gespeichert, um die Größe der ausführbaren Datei einzuschränken, Speicherplatz auf dem Datenträger zu sparen und den Zeitaufwand für das Laden der Daten zu verkürzen. Diese Methodik ermöglicht außerdem die Verteilung der ausführbaren Datei, ohne diese wichtigen Informationen offenzulegen, was das Programm leichter umkehren könnte.

Erstellen Sie zum Erstellen einer PDB-Datei die ausführbare Datei mit Debuginformationen gemäß den Anweisungen für die Buildtools.

Die dbghelp-API kann PDB verwenden, um die folgenden Informationen zu erhalten.

-   publics und Exporte
-   globale Symbole
-   lokale Symbole
-   Typdaten
-   Quelldateien
-   Zeilennummern

## <a name="dbg-files-and-embedded-debug-information"></a>Dbg-Dateien und eingebettete Debuginformationen

Frühere Versionen des Microsoft-Toolsets, das zum Einbetten der Debuginformationen in die ausführbare Datei verwendet wird, werden jedoch normalerweise in eine separate Datei mit der Erweiterung. dbg entfernt. Dies wird häufig als *dbg* -Datei bezeichnet. Dbg-Dateien verwenden dasselbe PE-Dateiformat wie ausführbare Dateien.

Die dbghelp-API-Unterstützung für DBGs und eingebettete Debuginformationen ist begrenzt und umfasst Folgendes:

-   publics und Exporte
-   globale Symbole

 

 



