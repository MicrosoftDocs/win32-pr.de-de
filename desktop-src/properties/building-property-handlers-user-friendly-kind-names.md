---
description: Das Eigenschaften System enthält eine Eigenschaft mit dem Namen System. Kind, die Elemente entsprechend der Dateinamenerweiterung in Typen unterteilt und die Endbenutzer leicht mit identifizieren können.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Verwenden von Kind-Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344818"
---
# <a name="using-kind-names"></a>Verwenden von Kind-Namen

Das-Eigenschaften System enthält eine Eigenschaft mit dem Namen `System.Kind` , die Elemente entsprechend der Dateinamenerweiterung in Typen unterteilt und die Endbenutzer leicht mit identifizieren können.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zur System. Kind-Eigenschaft](#about-the-systemkind-property)
-   [Kind-Wert Hierarchie und Registrierung](#kind-value-hierarchy-and-registration)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-the-systemkind-property"></a>Informationen zur System. Kind-Eigenschaft

Art wurde in Windows Vista eingeführt, um einen benutzerfreundlicheren Begriff "Dateityp" auszudrücken. Die `System.Kind` -Eigenschaft teilt Elemente in Typen auf und gibt einen Namen an, mit dem Endbenutzer identifizieren können (z. b. Dokumente, Musik, Bilder usw.). Daher sind Kind-Namen als benutzerfreundlich bekannt. Da die `System.Kind` -Eigenschaft auf denselben Wert für Elemente desselben Dateityps festgelegt ist und Elemente, die ähnliche Merkmale aufweisen, mit einer gemeinsamen Eigenschaft verknüpft werden, können das System und der Benutzer für die Gruppe als Ganzes agieren. Beispielsweise kann die- `System.Kind` Eigenschaft verwendet werden, um eine Suche auf Elemente einer bestimmten Art zu beschränken, die relevantesten Eigenschaften für ein Element in der Inhaltsansicht anzuzeigen oder ähnliche Elemente zu gruppieren.

Da Kind eine mehrwertige Zeichen folgen Eigenschaft ist, können Sie einen- `audio;video` Wert oder einen- `link;document` Wert haben. Ein- `System.Kind` Wert ist eine geordnete Liste von Zeichen folgen Werten. In einigen Fällen gibt es möglicherweise nur ein Element in der Liste. In anderen Fällen kann ein Element zu mehr als einer Art gehören. Ein Beispiel für ein Element, das zu mehr als einer Art gehört, finden Sie im Beispiel für den Registrierungsschlüssel in diesem Thema. Die Zeichen folgen Werte stammen aus einem vordefinierten Satz bekannter Werte. Die Werte werden mithilfe der Groß-/Kleinschreibung und der Gebiets Schema spezifischen Zeichen folgen Vergleichsfunktionen verglichen. Diese Zeichen folgen sind nicht lokalisiert.

Einige Arten von Namen sind bereits Eigenschaften und layoutmustern zugeordnet. Beispielsweise werden Elementen, `Kind.Picture` die mit-und-Elementen verknüpft sind, die mit verknüpft sind `Kind.Document` , andere Eigenschaften angezeigt, auch wenn Sie sich in derselben Ansicht befinden, aufgrund der Eigenschaften und Layoutmuster, die diesen beiden Namen bereits zugeordnet sind. Jede Elementart kann einem von vier eindeutigen layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definiert, die für jedes Element und dessen Layout angezeigt werden. Weitere Informationen finden Sie unter [Content View based on the file type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Kind-Wert Hierarchie und Registrierung

Ein `Kind` Wert muss einen der Werte in der folgenden Liste darstellen.

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

Eigenschaften Handler können Ihre `System.Kind` Eigenschaft statisch über die Registrierung deklarieren, oder Sie können den Wert dynamisch über Ihren Code bereitstellen, wie dies bei einer Standard Eigenschaft der Fall wäre.

Um die Eigenschaft statisch zu definieren `Kind` , wird unter dem **kindmap** -Registrierungsschlüssel ein **reg \_ SZ** -Wert Eintrag hinzugefügt, wie im folgenden Beispiel gezeigt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

Beachten Sie, dass `Kind` ein einzelner Wert oder mehrere Werte in einer durch Semikolons getrennten Zeichenfolge sein kann. Wenn Sie mehrere Werte angeben, wird der spezifischere `Kind` Wert zuerst mit dem am wenigsten spezifischen Wert aufgelistet. Im Beispiel wird "Contact" zuerst benannt, da es hierarchisch spezifischer als die Kommunikation ist. Das Wert **Element** wird angenommen und sollte nicht explizit explizit angegeben werden.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Eine Referenz Dokumentation zu Eigenschaften finden Sie unter [System. Kind](./props-system-kind.md) und [System. kindtext](./props-system-kindtext.md).
-   Weitere Informationen zum Erstellen neuer oder vorhandener Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaften Handlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Eigenschaften Listen](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
