---
description: Nachdem Sie Ihre Eigenschaftsstrategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der benutzeroberfläche Windows Explorer angezeigt werden sollen und wo.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Verwenden von Eigenschaftenlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72289612d61ebfb198ec0f2ee3d4a7d206209e91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477396"
---
# <a name="using-property-lists"></a>Verwenden von Eigenschaftenlisten

Nachdem Sie Ihre Eigenschaftsstrategie bewertet haben, müssen Sie bestimmen, welche Eigenschaften in der benutzeroberfläche Windows Explorer angezeigt werden sollen und wo. Es gibt verschiedene Speicherorte, an denen Eigenschaften schreibgeschützt angezeigt werden. Die Eigenschaftenbearbeitung ist dagegen nur im Dialogfeld **Eigenschaften** aktiviert. Dieses Dialogfeld kann entweder über den Link **Eigenschaften bearbeiten** im **Vorschaubereich** oder über das Kontextmenü eines Elements aufgerufen werden.

Bei den Eigenschaftenlisten handelt es sich um durch Semikolons getrennte Zeichenfolgen mit der folgenden Form.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



Das einzige derzeit verfügbare Flag wird in der folgenden Tabelle angezeigt.



| Flag | Beschreibung                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Zeigen Sie die Eigenschaft nicht wie im Registrierungsschlüsselwert **PreviewDetailsbewiesen** im **Vorschaubereich** an. Sehen Sie sich das Beispiel an, das auf die nächste Tabelle folgt, wenn der Wert dieser Eigenschaft nicht festgelegt ist. |



 

Nachdem Sie eine Eigenschaftenliste definiert haben, können Sie diese Zeichenfolge über das [Standardmäßige Shell-Dateizuordnungssystem](../shell/fa-file-types.md) unter HKEY CLASSES ROOT in der Registrierung **\_ \_ speichern.** In der folgenden Tabelle sind die Werte für die Eigenschaftenlisten zusammengefasst, die unter dem Registrierungsschlüssel für eine bestimmte Dateinamenerweiterung zugewiesen werden können.




| Wert | BESCHREIBUNG | 
|-------|-------------|
| FullDetails | Eigenschaften werden auf der Registerkarte <strong>Details</strong> des Dialogfelds <strong>Eigenschaften</strong> angezeigt. Dies ist die vollständige Liste der Eigenschaften, die vom Dateityp unterstützt werden. | 
| PreviewDetails | Eigenschaften werden im <strong>Vorschaubereich</strong>angezeigt. | 
| PreviewTitle | Eigenschaften werden im Titelbereich des <strong>Vorschaubereichs</strong> neben der Miniaturansicht für das Element angezeigt. Die maximale Anzahl von Einträgen beträgt 3. Wenn die Eigenschaftenliste mehr als die maximal zulässige Anzahl enthält, werden die restlichen Einträge ignoriert. | 
| TileInfo | Eigenschaften werden angezeigt, wenn sich die Listenansicht im <strong>Ansichtsmodus Kacheln</strong> befindet. Die maximale Anzahl von Einträgen beträgt 3. Wenn die Eigenschaftenliste mehr als die maximal zulässige Anzahl enthält, werden die restlichen Einträge ignoriert.<blockquote>[!Note]<br />Dieser Wert war in Windows XP vorhanden.</blockquote><br /> | 
| ExtendedTileInfo | Eigenschaften werden für ein Element angezeigt, <strong></strong> wenn sich die Listenansicht im Erweiterten Kachelansichtsmodus befindet. | 
| InfoTip | Eigenschaften werden in einer Infotip angezeigt, wenn ein Benutzer auf ein Element zeigt.<blockquote>[!Note]<br />Dieser Wert war in Windows XP vorhanden.</blockquote><br /> | 
| Quicktip | Eigenschaften werden angezeigt, wenn es schwierig ist, Eigenschaften direkt aus einem Element abzurufen, z. B. wenn über eine langsame Netzwerkverbindung auf das Element zugegriffen werden muss. Es wird empfohlen, dass die hier genannten Eigenschaften wie Typ oder Größe nicht den Dateistream öffnen müssen, um ihren Wert zu bestimmen.<blockquote>[!Note]<br />Dieser Wert war in Windows XP vorhanden.</blockquote><br /> | 




 

Im folgenden Beispiel wird der PreviewDetails-Wert für einen Rezeptdateityp mithilfe einer ProgID von **RecipeKey** definiert.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Wie im Thema [Shell-Dateizuordnung](../shell/fa-file-types.md) erläutert, können Dateizuordnungen für die spezifischste für die allgemeinste Form beschrieben werden. Das spezifischste Formular ist die Erweiterung für einzelne Dateierweiterungen, und das allgemeinste Formular ist ein Schlüssel, der für alle Dateien und Dateiordner gilt. Zwischen diesen beiden Extremen können Sie auch eine [PROGID](../shell/fa-progids.md) definieren, die einen Satz von Dateinamenerweiterungen gruppiert (z. B. .jpg- und JPEG-Typen, die als **jpegfile** gruppiert sind). Wenn Sie Eigenschaftenlisten definieren, sollten Sie diese für ProgIDs oder in einigen Fällen für bestimmte Dateinamenerweiterungen definieren. Vermeiden Sie es, sich auf allgemeine Einträge wie den **AllFileSystemObjects-Schlüssel** zu verlassen.

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

 

 
