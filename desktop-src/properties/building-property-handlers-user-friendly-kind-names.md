---
description: Das Eigenschaftensystem enthält eine Eigenschaft namens System.Kind, die Elemente entsprechend der Dateinamenerweiterung in Typen aufteilt und mit der sich Endbenutzer leicht identifizieren können.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Verwenden von Kind-Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d5f1432e7680cfed63c2c210375f3b7a300fae4563ca308a3b25b8751fb139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971099"
---
# <a name="using-kind-names"></a>Verwenden von Kind-Namen

Das Eigenschaftensystem enthält eine Eigenschaft mit dem Namen `System.Kind` , die Elemente entsprechend der Dateinamenerweiterung in Typen aufteilt und mit der sich Endbenutzer leicht identifizieren können.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zur System.Kind-Eigenschaft](#about-the-systemkind-property)
-   [Hierarchie und Registrierung von Kind-Werten](#kind-value-hierarchy-and-registration)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-the-systemkind-property"></a>Informationen zur System.Kind-Eigenschaft

Kind wurde in Windows Vista eingeführt, um ein benutzerfreundlicheres Konzept des Dateityps auszudrücken. Die `System.Kind` -Eigenschaft unterteilt Elemente in Typen und stellt einen Kind-Namen bereit, mit dem Endbenutzer identifizieren können, z. B. Dokumente, Musik, Bilder usw. Daher werden Kind-Namen als benutzerfreundliche Namen bezeichnet. Da die `System.Kind` -Eigenschaft für Elemente desselben Dateityps auf den gleichen Wert festgelegt ist und Elemente mit ähnlichen Eigenschaften einer gemeinsamen Eigenschaft zuweist, können das System und der Benutzer für die gruppe als Ganzes agieren. Beispielsweise kann die `System.Kind` -Eigenschaft verwendet werden, um eine Suche auf Elemente einer bestimmten Art zu beschränken, die relevantesten Eigenschaften für ein Element in der Inhaltsansicht anzuzeigen oder ähnliche Elemente zu gruppieren.

Da Kind eine Zeichenfolgeneigenschaft mit mehreren Werten ist, können Sie über einen - oder einen `audio;video` `link;document` Kind-Wert verfügen. Ein `System.Kind` -Wert ist eine sortierte Liste von Zeichenfolgenwerten. In einigen Fällen gibt es möglicherweise nur ein Element in dieser Liste. In anderen Fällen kann ein Element zu mehreren Arten gehören. Ein Beispiel für ein Element, das zu mehr als einer Art gehört, finden Sie im Registrierungsschlüsselbeispiel in diesem Thema. Die Zeichenfolgenwerte stammen aus einem vordefinierten Satz bekannter Werte. Die Werte werden mithilfe von Zeichenfolgenvergleichsfunktionen ohne Unterscheidung nach Groß-/Kleinschreibung und gebietsschemaunabhängig verglichen. Diese Zeichenfolgen werden nicht lokalisiert.

Einige Kind-Namen sind bereits Eigenschaften und Layoutmustern zugeordnet. Beispielsweise zeigen Elemente, die zugeordnet `Kind.Picture` sind, und Elemente, die zugeordnet `Kind.Document` sind, unterschiedliche Eigenschaften an, auch wenn sie sich in derselben Ansicht befinden. Dies liegt an den Eigenschaften und Layoutmustern, die diesen beiden Kind-Namen bereits zugeordnet sind. Jede Elementart kann einem von vier eindeutigen Layoutmustern zugeordnet werden, die die Anzahl der Eigenschaften definieren, die für jedes Element und dessen Layout angezeigt werden. Weitere Informationen finden Sie unter [Inhaltsansicht basierend auf dem Dateityp oder der Art-Zuordnung.](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85))

## <a name="kind-value-hierarchy-and-registration"></a>Hierarchie und Registrierung von Kind-Werten

Ein `Kind` -Wert muss einen der Werte in der folgenden Liste darstellen.

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

Eigenschaftenhandler können ihre `System.Kind` Eigenschaft statisch über die Registrierung deklarieren, oder sie können den Wert dynamisch über ihren Code bereitstellen, wie sie es mit einer Standardeigenschaft würden.

Um die Eigenschaft statisch zu `Kind` definieren, wird ein **REG \_ SZ-Werteintrag** unter dem **KindMap-Registrierungsschlüssel** hinzugefügt, wie im folgenden Beispiel gezeigt.

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

Beachten Sie, dass ein `Kind` einzelner Wert oder mehrere Werte in einer durch Semikolons getrennten Zeichenfolge sein können. Wenn Sie mehrere Werte bereitstellen, wird der spezifischste `Kind` Wert zuerst mit dem am wenigsten spezifischen Wert aufgeführt. Im Beispiel wird Contact zuerst benannt, da er hierarchisch spezifischer als Communications ist. Der Wert **Item** wird angenommen und sollte nicht explizit angegeben werden.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Eine Referenzdokumentation zu Eigenschaften finden Sie unter [System.Kind](./props-system-kind.md) und [System.KindText.](./props-system-kindtext.md)
-   Weitere Informationen zum Erstellen neuer oder verwenden vorhandener Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaftenhandlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Eigenschaftenlisten](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaftenhandlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaftenhandlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
