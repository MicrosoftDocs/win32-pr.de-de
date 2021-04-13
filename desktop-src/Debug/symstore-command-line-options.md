---
description: Die folgenden Syntax Formen werden für SymStore-Transaktionen unterstützt. Der erste Parameter muss immer "Add" oder "del" lauten. Die Reihenfolge der anderen Parameter spielt keine Rolle.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Optionen für SymStore-Command-Line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b69cdca9ee74cf01041375f26b2e151dc3ec5d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351948"
---
# <a name="symstore-command-line-options"></a>Optionen für SymStore-Command-Line

Die folgenden Syntax Formen werden für SymStore-Transaktionen unterstützt. Der erste Parameter muss immer "Add" oder "del" lauten. Die Reihenfolge der anderen Parameter spielt keine Rolle.

**SymStore hinzufügen** \[ **/l** **/o** **/p** **/r** **/Compress** \] \[ **-: msg** *Message* \] \[ **-: rel** \] \[ **-: norefs** \] **/f** *File* **/s** *Store* **/t** *Product* \[ **/v** *Version* \] \[ **/c** *comment* \] \[ **/d** *logfile*\]

**SymStore hinzufügen** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-: rel** \] \[ **-: norefs** \] **/g** *share* **/f** *File* **/x** *Indexfile* \[ **/d** *logfile*\]

**SymStore hinzufügen** \[ **/o** **/Compress** \] \[ **/p** \[ **-: msg** \| *Message* \] \[ **-: rel** \] \[ **-: norefs** \] \] **/y** *Indexfile* **/g** *share* **/s** *Store* **/t** *Product* \[ **/v** *Version* \] \[ **/c** *comment* \] \[ **/d** *logfile*\]

**SymStore-Abfrage** \[ **/o** **/r** \] **/f** *File* **/s** *Store* \[ **/d** *logfile*\]

**SymStore-** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *logfile*\]

**SymStore** **/?**



| Parameter      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Bewirkt, dass SymStore neue Indizierungs Informationen an eine vorhandene Indexdatei anfügt. (Diese Option wird nur mit der/x-Option verwendet.)                                                                                                                                                                                                                                                                                 |
| /c- *Kommentar*   | Gibt einen Kommentar für die Transaktion an.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Bewirkt, dass SymStore eine komprimierte Version der einzelnen Dateien erstellt, die in den Symbol Speicher kopiert werden, anstatt eine nicht komprimierte Kopie der Datei zu verwenden. Diese Option ist nur gültig, wenn Dateien und keine Zeiger gespeichert werden, und kann nicht mit der/p-Option verwendet werden.                                                                                                                                                              |
| /d *logfile*   | Gibt eine Protokolldatei an, die für die Befehlsausgabe verwendet werden soll. Wenn diese nicht eingeschlossen ist, werden Transaktionsinformationen und andere Ausgaben an stdout gesendet.                                                                                                                                                                                                                                                                     |
| /f- *Datei*      | Gibt einen oder mehrere Dateipfade (oder Verzeichnisse) an, die hinzugefügt werden sollen. Wenn ein angegebener Dateipfad mit dem Symbol "@" beginnt, wird eine [Antwortdatei](../midl/response-files.md) mit einer Liste der hinzu zufügenden Dateien erwartet (ein Dateipfad pro Zeile).                                                                                                                                             |
| /g- *Freigabe*     | Gibt den Server und die Freigabe an, in der die Symbol Dateien ursprünglich gespeichert wurden. Bei Verwendung mit/f sollte die *Freigabe* mit dem Anfang des *dateispezifizierers* identisch sein. Bei Verwendung mit/y sollte die *Freigabe* der Speicherort der ursprünglichen Symbol Dateien (nicht der Indexdatei) sein. Auf diese Weise können Sie diesen Teil des Dateipfads später ändern, wenn Sie die Symbol Dateien auf einen anderen Server und eine andere Freigabe verschieben. |
| /i- *ID*        | Gibt die Transaktions-ID-Zeichenfolge an.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Ermöglicht es, dass sich die Datei in einem lokalen Verzeichnis und nicht in einem Netzwerkpfad befinden kann. (Diese Option wird nur mit der/p-Option verwendet.)                                                                                                                                                                                                                                                                                        |
| /o             | Bewirkt, dass SymStore Ausführliche Ausgaben anzeigt.                                                                                                                                                                                                                                                                                                                                                                   |
| /p             | Bewirkt, dass SymStore einen Zeiger auf die Datei anstatt auf die Datei selbst speichert.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Veranlasst SymStore, Dateien oder Verzeichnisse rekursiv hinzuzufügen.                                                                                                                                                                                                                                                                                                                                                     |
| /s- *Speicher*     | Gibt das Stammverzeichnis für den Symbol Speicher an.                                                                                                                                                                                                                                                                                                                                                           |
| /t- *Produkt*   | Gibt den Namen des Produkts an.                                                                                                                                                                                                                                                                                                                                                                           |
| /v- *Version*   | Gibt die Version des Produkts an.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *Indexfile* | Bewirkt, dass SymStore die eigentlichen Symbol Dateien nicht speichert. Stattdessen zeichnet SymStore Informationen in der *Indexfile* auf, mit denen SymStore zu einem späteren Zeitpunkt auf die Symbol Dateien zugreifen kann.                                                                                                                                                                                                                         |
| /y *Indexfile* | Bewirkt, dass SymStore die Daten aus einer Datei liest, die mit/x. erstellt wurde.                                                                                                                                                                                                                                                                                                                                                |
| -: Meldung Nachricht  | Fügt die angegebene Meldung zu jeder Datei hinzu. (Diese Option kann nur verwendet werden, wenn/p verwendet wird.)                                                                                                                                                                                                                                                                                                                     |
| -: Rel          | Ermöglicht, dass die Pfade in den Datei Zeigern relativ sind. Diese Option impliziert die Option/l. (Diese Option kann nur verwendet werden, wenn/p verwendet wird.)                                                                                                                                                                                                                                                                     |
| -: Norefs       | Lässt die Erstellung von Verweis Zeiger Dateien für die Dateien und Zeiger aus, die gespeichert werden. Diese Option ist nur während der ersten Erstellung eines Symbol Speicher gültig, wenn der zu ändernde Speicher mit dieser Option erstellt wurde.                                                                                                                                                                                      |
| /?             | Zeigt den Hilfetext für den Befehl "SymStore" an.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



