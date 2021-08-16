---
description: In diesem Thema wird eine neue Ansicht im Windows-Explorer beschrieben, die als Inhaltsansicht bezeichnet wird und den relevantesten Inhalt für jedes Element anzeigt.
title: Inhaltsansicht nach Dateityp oder Art
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 83f70649bd0eb022bde9cc4a8c69e0df162fe2551268f611390bae835409e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858712"
---
# <a name="content-view-by-file-type-or-kind"></a>Inhaltsansicht nach Dateityp oder Art

In diesem Thema wird eine neue Ansicht im Windows-Explorer beschrieben, die als Inhaltsansicht bezeichnet wird und den relevantesten Inhalt für jedes Element anzeigt. Mithilfe eines Satzes von Registrierungsschlüsseln können Elemente eine Eigenschaftenliste und ein Layout definieren, das die Shell für die Inhaltsansicht verwendet. Die Shell ruft die Registrierungsschlüssel mithilfe des [Zuordnungsarrays](fa-perceivedtypes.md)des Elements ab.

## <a name="how-does-the-content-view-work"></a>Wie funktioniert die Inhaltsansicht?

In Windows 7 und höher verwendet die Inhaltsansicht eine Größenänderungslogik, die Eigenschaften löscht, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften immer noch Platz haben, um klar lesbar zu sein. Der folgende Screenshot veranschaulicht die Inhaltsansicht von Suchergebnissen, die Musik, Bilder und Dokumente enthalten.

![Inhaltsansicht von Suchergebnissen mit Musik, Bildern und Dokumenten](images/content-view/contentviewsearchresults.png)

Einige Shell-Datenquellen verwenden standardmäßig die Inhaltsansicht, aber Benutzer können die Inhaltsansicht auswählen, indem sie im Windows Explorer auf die Schaltfläche **Steuerelement anzeigen** klicken. Eine Shell-Datenquelle erweitert den Shellnamespace und macht Elemente in einem Datenspeicher verfügbar. Die Elemente in einem Datenspeicher können vom Windows Search-System mithilfe eines Protokollhandlers indiziert werden.

## <a name="how-to-implement-the-content-view"></a>Implementieren der Inhaltsansicht

Beim Registrieren eines neuen [Dateityps](fa-file-types.md) oder [Protokollhandlers](../search/-search-3x-wds-extidx-prot-implementing.md)können Sie die Inhaltsansicht nutzen, indem Sie einen von zwei verschiedenen Ansätzen verwenden. Sie können einen vorhandenen Satz von Eigenschaften und ein Layoutmuster verwenden oder eine eigene Kombination erstellen.

Sie können einen Registrierungseintrag verwenden, um Ihren Dateityp oder Ihr Element einer vordefinierten [Art](../properties/building-property-handlers-user-friendly-kind-names.md)zuzuordnen. Dabei handelt es sich um eine Eigenschaft, die Sie sich als Inhaltskategorie vorstellen können. Indem Sie Ihren Dateityp oder Ihr Element bestimmten dieser Arten zuordnen, erben Sie automatisch die Layoutmuster und Eigenschaftenlisten der Inhaltsansicht von Kind. Windows definiert Layoutmuster und Eigenschaftenlisten der Inhaltsansicht für die folgenden Arten: Dokumente, E-Mail, Ordner, Musik, Bild und generisch. Diese Art von Zuordnung wird empfohlen. Damit können Sie die konsistente Oberfläche bereitstellen, die ein Benutzer für ähnliche Elemente erwartet.

Weitere Informationen finden Sie unter [Dateitypen](fa-file-types.md) und [Typnamen](../properties/building-property-handlers-user-friendly-kind-names.md) und [Registrieren eines eindeutigen Inhaltsansichtssatzes mit Eigenschaften und Layoutmustern für den Dateityp oder das Element](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Weitere Ressourcen

-   Eine Referenzdokumentation zu Eigenschaften finden Sie unter [System.Kind](../properties/props-system-kind.md)und [System.KindText](../properties/props-system-kindtext.md).
-   Eine PropList-Referenzdokumentation finden Sie unter [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)und [System.PropList.ContentViewModeForSearch.](../properties/props-system-proplist-contentviewmodeforsearch.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Dateitypüberprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 
