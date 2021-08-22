---
description: Entwickler von Windows Installer-Paketen bemerken möglicherweise, dass ihre .msi-Dateien nach wiederholten Bearbeitungen und Speichern größer als erwartet werden.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reduzieren der Größe einer .msi-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b41cfeb949299ff4d80147fe09437cbfd708a4279bb43189c2528c495eb391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534089"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Reduzieren der Größe einer .msi-Datei

Entwickler von Windows Installer-Paketen bemerken möglicherweise, dass ihre .msi-Dateien nach wiederholten Bearbeitungen und Speichern größer als erwartet werden. Windows Das Installationsprogramm .msi Dateien sind Verbunddateien, die Speicher und Streams enthalten und einige der gleichen Speichereinschränkungen wie OLE-Dokumentdateien aufweisen. Wenn Sie die gleiche .msi Datei immer wieder bearbeiten und speichern, wird in der Datei speicherplatzvergewendet. Dies betrifft nur Autoren .msi Dateien und hat keine Auswirkungen auf Windows Installer-Benutzer. Entwickler möchten diesen ungenutzten Speicherplatz möglicherweise entfernen, bevor sie ihre endgültige .msi-Datei versenden.

Um ungenutzten Speicherplatz zu entfernen und die endgültige Größe .msi Dateien zu reduzieren, haben Sie die folgenden Optionen.

-   Exportieren Sie alle Tabellen in der Datenbank in IDT-Dateien, und importieren Sie diese dann in eine neue Datenbank. Dadurch wird möglichst kompakter Speicher erzeugt.
-   Verwenden Sie ein Softwarehilfsprogramm zum Komprimieren des Speicherplatzes von OLE-Dokumentdateien.

 

 



