---
description: Die folgenden Syntaxformen werden für SymStore-Transaktionen unterstützt. Der erste Parameter muss immer add oder del sein. Die Reihenfolge der anderen Parameter spielt keine Rolle.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: SymStore Command-Line-Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc166ab82fc40ad11eb9b014a003dc793f3bb7cc1d70792370bd175c68802417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572980"
---
# <a name="symstore-command-line-options"></a>SymStore Command-Line-Optionen

Die folgenden Syntaxformen werden für SymStore-Transaktionen unterstützt. Der erste Parameter muss immer add oder del sein. Die Reihenfolge der anderen Parameter spielt keine Rolle.

**symstore add** \[ **/l** **/o** **/p** **/r /compress**  \] \[ **-:MSG** *Message* \] \[ **-:REL** \] \[ **-:NOREFS** \] **/f** *File* **/s** *Store* **/t** *Product* \[ **/v** *Version* \] \[ **/c** *Comment* \] \[ **/d** *LogFile*\]

**symstore add** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-:REL** \] \[ **-:NOREFS** \] **/g** *Freigabe* **/f** *Datei* **/x** *IndexFile* \[ **/d** *LogFile*\]

**symstore add** \[ **/o** **/compress** \] \[ **/p** \[ **-:MSG** \| *Message* \] \[ **-:REL** \] \[ **-:NOREFS** \] \] **/y** *IndexFile* **/g** *Share* **/s** *Store* **/t** *Product* \[ **/v** *Version* \] \[ **/c** *Comment* \] \[ **/d** *LogFile*\]

**Symstore-Abfrage** \[ **/o** **/r** \] **/f** *Datei* **/s** *Store* \[ **/d** *LogFile*\]

**symstore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *LogFile*\]

**symstore** **/?**



| Parameter      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Bewirkt, dass SymStore neue Indizierungsinformationen an eine vorhandene Indexdatei anfügt. (Diese Option wird nur mit der Option /x verwendet.)                                                                                                                                                                                                                                                                                 |
| /c *Comment*   | Gibt einen Kommentar für die Transaktion an.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Bewirkt, dass SymStore eine komprimierte Version jeder Datei erstellt, die in den Symbolspeicher kopiert wird, anstatt eine unkomprimierte Kopie der Datei zu verwenden. Diese Option ist nur beim Speichern von Dateien und nicht bei Zeigern gültig und kann nicht mit der Option /p verwendet werden.                                                                                                                                                              |
| /d *LogFile*   | Gibt eine Protokolldatei an, die für die Befehlsausgabe verwendet werden soll. Wenn dies nicht enthalten ist, werden Transaktionsinformationen und andere Ausgaben an stdout gesendet.                                                                                                                                                                                                                                                                     |
| */f-Datei*      | Gibt einen oder mehrere hinzuzufügende Dateipfade (oder Verzeichnisse) an. Wenn ein angegebener Dateipfad mit einem @-Symbol beginnt, wird eine [Antwortdatei](../midl/response-files.md) mit einer Liste der hinzuzufügenden Dateien (ein Dateipfad pro Zeile) erwartet.                                                                                                                                             |
| /g *Freigabe*     | Gibt den Server und die Freigabe an, auf dem die Symboldateien ursprünglich gespeichert wurden. Bei Verwendung mit /f sollte *Die Freigabe* mit dem Anfang des *Dateispezifizierer* identisch sein. Bei Verwendung mit /y sollte *Freigabe* der Speicherort der ursprünglichen Symboldateien (nicht der Indexdatei) sein. Dadurch können Sie diesen Teil des Dateipfads später ändern, falls Sie die Symboldateien auf einen anderen Server und eine andere Freigabe verschieben. |
| /i *ID*        | Gibt die Transaktions-ID-Zeichenfolge an.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Ermöglicht, dass sich die Datei in einem lokalen Verzeichnis und nicht in einem Netzwerkpfad befindet. (Diese Option wird nur mit der Option /p verwendet.)                                                                                                                                                                                                                                                                                        |
| /o             | Bewirkt, dass SymStore eine ausführliche Ausgabe anzeigt.                                                                                                                                                                                                                                                                                                                                                                   |
| /p             | Bewirkt, dass SymStore anstelle der Datei selbst einen Zeiger auf die Datei speichert.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Bewirkt, dass SymStore Dateien oder Verzeichnisse rekursiv hinzufügt.                                                                                                                                                                                                                                                                                                                                                     |
| /s *Store*     | Gibt das Stammverzeichnis für den Symbolspeicher an.                                                                                                                                                                                                                                                                                                                                                           |
| /t *Product*   | Gibt den Namen des Produkts an.                                                                                                                                                                                                                                                                                                                                                                           |
| */v-Version*   | Gibt die Version des Produkts an.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *IndexFile* | Bewirkt, dass SymStore die eigentlichen Symboldateien nicht speichert. Stattdessen zeichnet SymStore Informationen in der *IndexFile* auf, mit denen SymStore zu einem späteren Zeitpunkt auf die Symboldateien zugreifen kann.                                                                                                                                                                                                                         |
| /y *IndexFile* | Bewirkt, dass SymStore die Daten aus einer mit /x erstellten Datei liest.                                                                                                                                                                                                                                                                                                                                                |
| -:MSG-Nachricht  | Fügt jeder Datei die angegebene Meldung hinzu. (Diese Option kann nur verwendet werden, wenn /p verwendet wird.)                                                                                                                                                                                                                                                                                                                     |
| -:REL          | Lässt zu, dass die Pfade in den Dateizeigern relativ sind. Diese Option impliziert die Option /l. (Diese Option kann nur verwendet werden, wenn /p verwendet wird.)                                                                                                                                                                                                                                                                     |
| -:NOREFS       | Lässt die Erstellung von Verweiszeigerdateien für die gespeicherten Dateien und Zeiger aus. Diese Option ist nur während der ersten Erstellung eines Symbolspeichers gültig, wenn der geänderte Speicher mit dieser Option erstellt wurde.                                                                                                                                                                                      |
| /?             | Zeigt Hilfetext für den SymStore-Befehl an.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



