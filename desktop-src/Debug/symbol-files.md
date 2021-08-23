---
description: Normalerweise werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Symboldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610e289a64ed807a26086f12780b45bc35ea65464946ec81a07e4169515d1132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642180"
---
# <a name="symbol-files"></a>Symboldateien

Normalerweise werden Debuginformationen in einer Symboldatei gespeichert, die von der ausführbaren Datei getrennt ist. Die Implementierung dieser Debuginformationen hat sich im Laufe der Jahre geändert, und die folgende Dokumentation enthält Anleitungen zu diesen verschiedenen Implementierungen.

## <a name="pdb-files"></a>PDB-Dateien

Alle modernen Versionen der Microsoft-Compiler speichern Debuginformationen zu einer kompilierten ausführbaren Datei in einer *separaten* Programmdatenbankdatei (PDB). Diese Datei wird häufig als *PDB bezeichnet.* Die Daten werden in einer separaten Datei von der ausführbaren Datei gespeichert, um die Größe der ausführbaren Datei zu begrenzen, Speicherplatz auf dem Datenträger zu sparen und die Zeit zu reduzieren, die zum Laden der Daten benötigt wird. Diese Methodik ermöglicht auch die Verteilung der ausführbaren Datei, ohne diese wichtigen Informationen offenlegen zu müssen, wodurch das Programm einfacher reverse engineering möglich ist.

Um eine PDB-Datei zu erstellen, erstellen Sie Ihre ausführbare Datei mit Debuginformationen gemäß den Anweisungen für Ihre Buildtools.

Die DbgHelp-API kann PDBs verwenden, um die folgenden Informationen zu erhalten.

-   Publics und Exporte
-   Globale Symbole
-   Lokale Symbole
-   Typdaten
-   Quelldateien
-   Zeilennummern

## <a name="dbg-files-and-embedded-debug-information"></a>DBG-Dateien und eingebettete Debuginformationen

Frühere Versionen des Microsoft-Toolsets, die zum Einbetten der Debuginformationen in die ausführbare Datei verwendet wurden, wurden jedoch normalerweise in eine separate Datei mit der Erweiterung .dbg entfernt. Dies wird häufig als *DBG-Datei* bezeichnet. DBG-Dateien verwenden das gleiche PE-Dateiformat wie ausführbare Dateien.

Die DbgHelp-API-Unterstützung für DBGs und eingebettete Debuginformationen ist eingeschränkt und umfasst Folgendes.

-   Publics und Exporte
-   Globale Symbole

 

 



