---
description: In diesem Thema wird eine neue Ansicht in Windows Explorer beschrieben, die als Inhaltsansicht bezeichnet wird, in der der relevanteste Inhalt für jedes Element angezeigt wird.
title: Inhaltsansicht nach Dateityp oder-Art
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757362"
---
# <a name="content-view-by-file-type-or-kind"></a>Inhaltsansicht nach Dateityp oder-Art

In diesem Thema wird eine neue Ansicht in Windows Explorer beschrieben, die als Inhaltsansicht bezeichnet wird, in der der relevanteste Inhalt für jedes Element angezeigt wird. Mithilfe eines Satzes von Registrierungs Schlüsseln können Elemente eine Eigenschaften Liste und ein Layout definieren, die von der Shell für die Inhaltsansicht verwendet werden. Die Shell Ruft die Registrierungsschlüssel mithilfe des Zuordnungs [Arrays](fa-perceivedtypes.md)des Elements ab.

## <a name="how-does-the-content-view-work"></a>Wie funktioniert die Inhaltsansicht?

In Windows 7 und höher wird in der Inhaltsansicht eine Logik zur Größenänderung verwendet, die Eigenschaften löscht, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften weiterhin Platz aufweisen, um eindeutig lesbar zu sein. Der folgende Screenshot veranschaulicht die Inhaltsansicht von Suchergebnissen, die Musik, Bilder und Dokumente enthalten.

![Inhaltsansicht von Suchergebnissen mit Musik, Bildern und Dokumenten](images/content-view/contentviewsearchresults.png)

Einige shelldatenquellen verwenden die Inhaltsansicht standardmäßig. Benutzer können jedoch die Inhaltsansicht auswählen, indem Sie im Windows-Explorer auf die Schaltfläche " **View Control** " klicken. Eine shelldatenquelle erweitert den Shellnamespace und macht Elemente in einem Datenspeicher verfügbar. Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden.

## <a name="how-to-implement-the-content-view"></a>Implementieren der Inhaltsansicht

Wenn Sie einen neuen [Dateityp](fa-file-types.md) oder [Protokollhandler](../search/-search-3x-wds-extidx-prot-implementing.md)registrieren, können Sie die Inhaltsansicht nutzen, indem Sie einen der beiden unterschiedlichen Ansätze verwenden. Sie können einen vorhandenen Satz von Eigenschaften und layoutmustern verwenden, oder Sie können eine eigene Kombination erstellen.

Sie können einen Registrierungs Eintrag verwenden, um den Dateityp oder das Element einem [vordefinierten Typ](../properties/building-property-handlers-user-friendly-kind-names.md)zuzuordnen, bei dem es sich um eine Eigenschaft handelt, die Sie als Inhaltskategorie betrachten können. Indem Sie den Dateityp oder das Element mit bestimmten dieser Art verknüpfen, erben Sie die Layoutmuster und Eigenschaften Listen der Inhaltsansicht dieser Art automatisch. Windows definiert Layoutmuster und Eigenschaften Listen für die Inhaltsansicht für die folgenden Arten: Dokumente, e-Mail, Ordner, Musik, Bild und generisch. Diese Art von Zuordnung wird empfohlen. Damit können Sie die konsistente Benutzer Leistung bereitstellen, die ein Benutzer für ähnliche Elemente erwartet.

Weitere Informationen finden Sie unter [Dateitypen](fa-file-types.md) und [Kind-Namen](../properties/building-property-handlers-user-friendly-kind-names.md) und [Registrieren eines eindeutigen Inhalts Ansichts Satzes von Eigenschaften und layoutmustern für den Dateityp oder das Element](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zur Eigenschafts Referenz Dokumentation finden Sie unter [System. Kind](../properties/props-system-kind.md)und [System. kindtext](../properties/props-system-kindtext.md).
-   Eine Referenz Dokumentation zur proplist finden Sie unter [System. proplist. contentviewmodeforbrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)und [System. proplist. contentviewmodeforsearch](../properties/props-system-proplist-contentviewmodeforsearch.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 
