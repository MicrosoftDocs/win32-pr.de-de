---
description: Nachdem Sie Ihre Eigenschafts Strategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der Windows-Explorer-Benutzeroberfläche angezeigt werden sollen und wo.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Verwenden von Eigenschaften Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959362"
---
# <a name="using-property-lists"></a>Verwenden von Eigenschaften Listen

Nachdem Sie Ihre Eigenschafts Strategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der Windows-Explorer-Benutzeroberfläche angezeigt werden sollen und wo. Es gibt verschiedene Speicherorte, an denen Eigenschaften schreibgeschützt angezeigt werden. Die Eigenschaften Bearbeitung hingegen ist nur im Dialogfeld " **Eigenschaften** " aktiviert. Dieses Dialogfeld kann entweder über den Link **Eigenschaften bearbeiten** im **Vorschaufenster** oder das Kontextmenü eines Elements aufgerufen werden.

Die Eigenschaften Listen sind durch Semikolons getrennte Zeichen folgen, die die folgende Form aufweisen.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



Das einzige derzeit verfügbare Flag ist in der folgenden Tabelle aufgeführt.



| Flag | Beschreibung                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Zeigen Sie die-Eigenschaft im **Vorschau** Bereich nicht an, wie im **previewdetails** -Registrierungsschlüssel Wert beschrieben. Sehen Sie sich das Beispiel an, das der nächsten Tabelle folgt, wenn der Wert dieser Eigenschaft nicht festgelegt ist. |



 

Nachdem Sie eine Eigenschaften Liste definiert haben, können Sie diese Zeichenfolge in der Registrierung über das standardmäßige [shelldateizuordnungssystem](../shell/fa-file-types.md) unter **HKEY \_ Classes \_ root speichern.** In der folgenden Tabelle werden die Werte für die Eigenschaften Listen zusammengefasst, die unter dem Registrierungsschlüssel für eine bestimmte Dateinamenerweiterung zugewiesen werden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Voll Details</td>
<td>Eigenschaften werden im Dialogfeld <strong>Eigenschaften</strong> auf der Registerkarte <strong>Details</strong> angezeigt. Dies ist die gesamte Liste der Eigenschaften, die vom Dateityp unterstützt werden.</td>
</tr>
<tr class="even">
<td>Previewdetails</td>
<td>Eigenschaften werden im <strong>Vorschaufenster</strong>angezeigt.</td>
</tr>
<tr class="odd">
<td>PreviewTitle</td>
<td>Eigenschaften werden im Titelbereich des <strong>Vorschau</strong> Bereichs neben der Miniaturansicht des Elements angezeigt. Die maximale Anzahl von Einträgen beträgt 3. Wenn die Eigenschaften Liste mehr als die maximal zulässige Zahl enthält, werden die restlichen Einträge ignoriert.</td>
</tr>
<tr class="even">
<td>TileInfo</td>
<td>Eigenschaften werden angezeigt, wenn sich die Listenansicht im <strong>Kachel</strong> Ansichtsmodus befindet. Die maximale Anzahl von Einträgen beträgt 3. Wenn die Eigenschaften Liste mehr als die maximal zulässige Zahl enthält, werden die restlichen Einträge ignoriert.
<blockquote>
[!Note]<br />
Dieser Wert war in Windows XP vorhanden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Extendedtileinfo</td>
<td>Eigenschaften werden für ein Element angezeigt, wenn sich die Listenansicht im <strong>erweiterten Kachel</strong> Ansichtsmodus befindet.</td>
</tr>
<tr class="even">
<td>InfoTip</td>
<td>Eigenschaften werden in einem InfoTipp angezeigt, wenn ein Benutzer auf ein Element zeigt.
<blockquote>
[!Note]<br />
Dieser Wert war in Windows XP vorhanden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickInfo</td>
<td>Eigenschaften werden angezeigt, wenn es schwierig ist, Eigenschaften direkt von einem Element abzurufen, z. b. wenn auf das Element über eine langsame Netzwerkverbindung zugegriffen werden muss. Es wird empfohlen, dass die hier genannten Eigenschaften, z. b. Typ oder Größe, nicht das Öffnen des Datei Datenstroms zum Ermitteln ihres Werts erfordern.
<blockquote>
[!Note]<br />
Dieser Wert war in Windows XP vorhanden.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Im folgenden Beispiel wird der previewdetails-Wert für einen. Rezept-Dateityp mithilfe einer ProgID von "Receive- **Key**" definiert.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Wie im Thema [Shell-Datei](../shell/fa-file-types.md) Zuordnung erläutert, können Dateizuordnungen für die spezifischsten der allgemeinsten Form beschrieben werden. Die spezifischere Form ist die einzelne Dateinamenerweiterung, und die allgemeinste Form ist ein Schlüssel, der für alle Dateien und Datei Ordner gilt. Zwischen diesen beiden extremen können Sie auch eine [ProgID](../shell/fa-progids.md) definieren, die eine Reihe von Dateinamen Erweiterungen gruppiert (z. t. jpg-und JPEG-Typen, die als **jpeer-Datei** gruppiert sind). Wenn Sie Eigenschaften Listen definieren, sollten Sie diese für ProgIDs oder in einigen Fällen für bestimmte Dateinamen Erweiterungen definieren. Vermeiden Sie die Verwendung von allgemeinen Einträgen, wie z. b. dem **AllFilesystemObjects** -Schlüssel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaften Handlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
