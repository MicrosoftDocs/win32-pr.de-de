---
description: Nachdem Sie Ihre Eigenschaftsstrategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften auf der Benutzeroberfläche des Windows Explorers angezeigt werden sollen und wo.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Verwenden von Eigenschaftenlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68dc3f25b1f0223e62a969a5b0846bcbdcaaef9fd93b45c654c367a0c1fc949d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119397820"
---
# <a name="using-property-lists"></a>Verwenden von Eigenschaftenlisten

Nachdem Sie Ihre Eigenschaftsstrategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften auf der Benutzeroberfläche des Windows Explorers angezeigt werden sollen und wo. Es gibt verschiedene Speicherorte, an denen Eigenschaften schreibgeschützt angezeigt werden. Die Bearbeitung von Eigenschaften ist dagegen nur im Dialogfeld **Eigenschaften** aktiviert. Dieses Dialogfeld kann entweder über  den Link Eigenschaften  bearbeiten im Vorschaubereich oder über das Kontextmenü eines Elements aufgerufen werden.

Die Eigenschaftenlisten sind durch Semikolons getrennte Zeichenfolgen, die das folgende Formular haben.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



Das einzige derzeit verfügbare Flag ist in der folgenden Tabelle aufgeführt.



| Flag | Beschreibung                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Zeigen Sie die Eigenschaft nicht im **Vorschaubereich an,** wie im **Registrierungsschlüsselwert PreviewDetails** gezeigt. Sehen Sie sich das Beispiel an, das auf die nächste Tabelle folgt, wenn der Wert dieser Eigenschaft nicht festgelegt ist. |



 

Nachdem Sie eine Eigenschaftenliste definiert haben, können Sie [](../shell/fa-file-types.md) diese Zeichenfolge über das Standardmäßige Shelldatei-Zuordnungssystem unter HKEY CLASSES ROOT in **der \_ Registrierung \_ speichern.** In der folgenden Tabelle sind die Werte für die Eigenschaftenlisten zusammengefasst, die unter dem Registrierungsschlüssel für eine bestimmte Dateierweiterung zugewiesen werden können.



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
<td>FullDetails</td>
<td>Eigenschaften werden im Dialogfeld Eigenschaften <strong></strong> auf der Registerkarte <strong>Details</strong> angezeigt. Dies ist die vollständige Liste der Eigenschaften, die der Dateityp unterstützt.</td>
</tr>
<tr class="even">
<td>PreviewDetails</td>
<td>Eigenschaften werden im <strong>Vorschaubereich angezeigt.</strong></td>
</tr>
<tr class="odd">
<td>PreviewTitle</td>
<td>Eigenschaften werden im Titelbereich des Vorschaubereichs neben <strong>der</strong> Miniaturansicht für das Element angezeigt. Die maximale Anzahl von Einträgen ist 3. Wenn die Eigenschaftenliste mehr als die maximal zulässige Anzahl enthält, werden die restlichen Einträge ignoriert.</td>
</tr>
<tr class="even">
<td>TileInfo</td>
<td>Eigenschaften werden angezeigt, wenn sich die Listenansicht im <strong>Ansichtsmodus Kacheln</strong> befindet. Die maximale Anzahl von Einträgen ist 3. Wenn die Eigenschaftenliste mehr als die maximal zulässige Anzahl enthält, werden die restlichen Einträge ignoriert.
<blockquote>
[!Note]<br />
Dieser Wert war in xp Windows vorhanden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>ExtendedTileInfo</td>
<td>Eigenschaften werden für ein Element angezeigt, wenn sich die Listenansicht im <strong>Ansichtsmodus Erweiterte Kachel</strong> befindet.</td>
</tr>
<tr class="even">
<td>InfoTip</td>
<td>Eigenschaften werden in einer Infotip angezeigt, wenn ein Benutzer auf ein Element zeigt.
<blockquote>
[!Note]<br />
Dieser Wert war in xp Windows vorhanden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Quicktip</td>
<td>Eigenschaften werden angezeigt, wenn es schwierig ist, Eigenschaften direkt aus einem Element abzurufen, z. B. wenn auf das Element über eine langsame Netzwerkverbindung zugegriffen werden muss. Es wird empfohlen, dass die hier genannten Eigenschaften, z. B. Typ oder Größe, nicht das Öffnen des Dateistreams erfordern, um ihren Wert zu bestimmen.
<blockquote>
[!Note]<br />
Dieser Wert war in xp Windows vorhanden.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Im folgenden Beispiel wird der PreviewDetails-Wert für einen Recipe-Dateityp definiert, indem eine ProgID von **RecipeKey verwendet wird.**

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Wie im Thema [Shelldateizuordnung](../shell/fa-file-types.md) erläutert, können Dateizuordnungen für die spezifischste für die allgemeinste Form beschrieben werden. Die spezifischste Form ist die Erweiterung für einzelne Dateien, und die generischste Form ist ein Schlüssel, der für alle Dateien und Dateiordner gilt. Zwischen diesen beiden Extremen können Sie auch eine [PROGID](../shell/fa-progids.md) definieren, die einen Satz von Dateierweiterungen zusammen gruppiert (z. B. .jpg- und JPEG-Typen, die als **JPEG-Datei gruppiert sind).** Wenn Sie Eigenschaftenlisten definieren, sollten Sie sie für ProgIDs oder in einigen Fällen für bestimmte Dateierweiterungen definieren. Vermeiden Sie es, sich auf allgemeine Einträge wie den **AllFileSystemObjects-Schlüssel zu** verlassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaftenhandlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Initialisieren von Eigenschaftenhandlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaftenhandlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
