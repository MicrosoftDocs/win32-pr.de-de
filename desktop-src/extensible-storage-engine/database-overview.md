---
description: Weitere Informationen finden Sie in der Übersicht über Datenbanken
title: Datenbankübersicht
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 473ffc7f11b3688f0f0904ae15a366ef7d6812d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565745"
---
# <a name="database-overview"></a>Datenbankübersicht


_**Gilt für:** Windows | Windows Server_

## <a name="database-overview"></a>Datenbankübersicht

Die ESE-Datenbank ist eine indizierte sequenzielle Zugriffsmethode (ISAM) zum Speichern und Abrufen von Daten. Eine ESE-Datenbank wird in einer einzelnen Datei gespeichert und besteht aus einer oder mehreren benutzerdefinierten Tabellen. Die Daten werden in den Datensätzen in der Tabelle mit einer oder mehreren benutzerdefinierten Spalten organisiert. Indizes, die erstellt werden, bieten eine andere Organisation für den gesamten Satz oder eine Teilmenge der Datensätze in der Tabelle. Mithilfe der ESE-API können Anwendungen Cursor erstellen, die Datensätze in der Datenbank in unterschiedlichen sequenziellen Aufträgen navigieren. Die Elemente der Tabelle sind unten definiert:

  - **Column**: bei der Spalte handelt es sich um ein Feld in der Tabelle, in dem eine bestimmte Art von Informationen gespeichert ist. Spalten können je nach verwendetem Datentyp oder variabler Länge korrigiert werden. Einige Spalten, wie z. b. markierte Spalten, nehmen keinen Speicherplatz auf, wenn **null** oder auf den Standardwert festgelegt ist, und können mehrere Werte enthalten.

  - **Datensätze**: ein Datensatz ist eine Auflistung von Spaltenwerten, die eine eindeutige Identität aufweisen, wie durch den Primärschlüssel definiert.

  - **Index**: der Index ist eine Auflistung von Schlüssel Spalten, die eine gespeicherte Reihenfolge von Datensätzen in der Tabelle definieren. Der gruppierte Index (primär Index) definiert die Reihenfolge, in der die Datensätze in der Tabelle gespeichert werden. Es können mehrere Indizes definiert werden, um unterschiedliche Sortierungen der durch Traversierung durch Datensätze in der Tabelle anzugeben. Ein Index kann auch den Satz von Datensätzen begrenzen, der basierend auf einfachen Kriterien (z. b. das vorhanden sein oder Fehlen eines bestimmten Schlüssel Spaltenwerts im Datensatz) sichtbar ist.

  - **Cursor**: der Cursor gibt den aktuellen Datensatz in der Tabelle an und navigiert zu Datensätzen in der Tabelle mit dem aktuellen Index. Der Cursor enthält auch Informationen zum Status des aktuell vorbereiteten Updates.

Spalten und Indizes können jederzeit der Tabelle hinzugefügt oder daraus entfernt werden. Obwohl mehrere Indizes definiert werden können, werden die Daten in der Tabelle physisch gespeichert und entsprechend der primär Index Definition in einer B +-Struktur logisch gruppiert. Jeder sekundäre Index wird in einer separaten B +-Struktur gespeichert, die nur logische Zeiger auf die eigentlichen Daten enthält, die in der primären Tabelle gespeichert sind. Wenn kein Index definiert ist, werden die Datensätze in der Tabelle in einer B +-Struktur in der Reihenfolge der Einfügevorgänge gespeichert und als sequenzieller Index bezeichnet.

Im folgenden Diagramm finden Sie ein Beispiel dafür, wie die Daten für die Tabelle gemäß dem primären Index in einer B +-Struktur gespeichert werden. Der primäre Index ist für Name und ID, und für die Büronummer des Mitarbeiters wird ein sekundärer Index erstellt. Die Einträge für den sekundären Index werden in einer separaten B +-Struktur gespeichert, die nur Zeiger auf die in der primären Tabelle gespeicherten Datensätze enthält. Die Office-Nummer 12348 in der sekundären Tabelle bezieht sich z. b. auf Datensatz 3 in der primären Tabelle. Datensatz 3 enthält die Spaltenwerte für den Mitarbeiter in Office 12348. Weitere Informationen finden Sie im Thema [Indizierung in der Tabelle](./indexing-in-the-table.md) .

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
