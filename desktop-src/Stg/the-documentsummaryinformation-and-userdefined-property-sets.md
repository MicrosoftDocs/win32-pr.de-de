---
title: Die documentsummaryinformation-und UserDefined-Eigenschaften Sätze
description: Ein "documentsummaryinformation"-und ein benutzerdefinierter Eigenschaften Satz ist eine Erweiterung für den Eigenschaften Satz für Zusammenfassungs Informationen. Beide Eigenschaften Sätze können gleichzeitig vorhanden sein.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- Documentsummaryinformation
- Benutzerdefinierte Eigenschaften Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515722"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Die documentsummaryinformation-und UserDefined-Eigenschaften Sätze

Ein " **documentsummaryinformation** "-und ein **benutzerdefinierter** Eigenschaften Satz ist eine Erweiterung für [den Eigenschaften Satz für Zusammenfassungs Informationen](the-summary-information-property-set.md). Beide Eigenschaften Sätze können gleichzeitig vorhanden sein.

Der Name des Streams, der den **documentsummaryinformation** -Eigenschaften Satz enthält, ist **" \\ 005documentsummaryinformation"**. Der Format Bezeichner (fmtid) für den **documentsummaryinformation** -Eigenschaften Satz ist **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

Die Deklaration für diesen Wert ist in den bereitgestellten Header Dateien als **fmtid \_ docsummaryinformation** verfügbar. Weitere Informationen finden Sie unter [Namen in IStorage](names-in-istorage.md), [Eigenschaften Satz für Zusammenfassungs Informationen](the-summary-information-property-set.md), [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) und [Format](format-identifiers.md)Bezeichner.

Dieser Stream verfügt auch über einen separaten Abschnitt für die benutzerdefinierten benutzerdefinierten Eigenschaften, wie in den Eigenschaften Sätzen **documentsummaryinformation** und **UserDefined** . Dieser Abschnitt wird in der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle als separater Eigenschaften Satz mit der folgenden fmtid angezeigt (verfügbar als **fmtid \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Diese beiden Eigenschaften Sätze sind die einzigen, für die ein einzelner Stream mehrere Eigenschaften Sätze enthalten kann. Die Tatsache, dass sich diese zwei Eigenschafts Sätze in einem einzigen Stream befinden, wirkt sich auf das Verhalten der **IPropertySetStorage** -Schnittstelle aus. Weitere Informationen finden Sie unter [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

In der folgenden Tabelle werden die hinzugefügten Eigenschaften für den **documentsummaryinformation** -und den **UserDefined** -Eigenschaften Satz aufgelistet. Wie im **SummaryInformation** -Eigenschaften Satz werden die Namen in der Regel nicht im Eigenschaften Satz gespeichert, sondern aus dem Eigenschaften Bezeichner abgeleitet.



| Eigenschaftenname      | Eigenschaftsbezeichner     | Eigenschafts Bezeichnerwert | Varianttyp                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Category           | **piddsi- \_ Kategorie**    | 0x00000002                | **VT \_ LPSTR**                     |
| PresentationTarget | **piddsi- \_ präformat**  | 0x00000003                | **VT \_ LPSTR**                     |
| Byte              | **piddsi \_ byteCount**   | 0x00000004                | **VT \_ I4**                        |
| Linien              | **piddsi \_ LineCount**   | 0x00000005                | **VT \_ I4**                        |
| Absätze         | **piddsi- \_ Parser**    | 0x00000006                | **VT \_ I4**                        |
| Folien             | **piddsi- \_ diascount**  | 0x00000007                | **VT \_ I4**                        |
| Notizen              | **piddsi- \_ noteCount**   | 0x00000008                | **VT \_ I4**                        |
| Hiddenfolien       | **piddsi \_ hiddencount** | 0x00000009                | **VT \_ I4**                        |
| Mmclips            | **piddsi \_ mmclipcount** | 0x0000000A                | **VT \_ I4**                        |
| Scalecrop          | **piddsi- \_ Skala**       | 0x0000000b                | **VT \_ bool**                      |
| Headingpaare       | **piddsi \_ headingpair** | 0x0000000c                | **VT \_ Variant** \| **VT- \_ Vektor** |
| Titlesofparts      | **piddsi \_ docparts**    | 0x0000000d                | **VT \_ Vector** \| **VT \_ LPSTR**   |
| Manager            | **piddsi- \_ Manager**     | 0x0000000e                | **VT \_ LPSTR**                     |
| Company            | **piddsi- \_ Unternehmen**     | 0x0000000f                | **VT \_ LPSTR**                     |
| Linksupdedate      | **piddsi \_ linksdirty**  | 0x00000010                | **VT \_ bool**                      |



 

Diese Eigenschaften haben folgende Verwendungsmöglichkeiten:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie
</dt> <dd>

Eine vom Benutzer eingegebene Text Zeichenfolge, die angibt, zu welcher Kategorie die Datei gehört (Memo, Vorschlag usw.). Es ist hilfreich, um Dateien desselben Typs zu suchen.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Zielformat für die Präsentation (35mm, Drucker, Video usw.).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Satz
</dt> <dd>

Die Anzahl von Bytes.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Betreff
</dt> <dd>

Anzahl der Zeilen.

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>355
</dt> <dd>

Anzahl von Absätzen.

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Führten
</dt> <dd>

Anzahl der Folien.

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Anmerkungen
</dt> <dd>

Anzahl der Seiten, die Notizen enthalten.

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>Hiddenfolien
</dt> <dd>

Anzahl der ausgeblendeten Folien.

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>Mmclips
</dt> <dd>

Anzahl der Sound-oder Videoclips.

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>Scalecrop
</dt> <dd>

Legen Sie diese Einstellung auf true (-1) fest, wenn die Skalierung der Miniaturansicht gewünscht wird. Wenn nicht festgelegt, ist das Zuschneiden erwünscht.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>Headingpaare
</dt> <dd>

Intern verwendete Eigenschaft, die die Gruppierung verschiedener Dokument Teile und die Anzahl der Elemente in jeder Gruppe angibt. Die Titel der Dokument Teile werden in der **titlesofparts** -Eigenschaft gespeichert. Die **headingpairs** -Eigenschaft wird als Vektor von Varianten in sich wiederholenden Paaren von **VT \_ LPSTR** (oder **VT \_ LPWSTR**) und **VT \_ I4** -Werten gespeichert. Der **VT \_ LPSTR** -Wert stellt einen Überschriften Namen dar, und der **VT \_ I4** -Wert gibt die Anzahl der Dokument Teile unter dieser Überschrift an.

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>Titlesofparts
</dt> <dd>

Namen der Dokument Teile.

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Dienst
</dt> <dd>

Manager des Projekts.

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Geschäfts
</dt> <dd>

Firmenname.

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>Linksupdedate
</dt> <dd>

Boolescher Wert, der angibt, ob die benutzerdefinierten Verknüpfungen für alle Anwendungen durch übermäßiges Rauschen behindert werden.

> [!Note]  
> Wie in 12,3 beschrieben. Das serialisierte Format für Eigenschafts Sätze der OLE 2,0-Entwurfs Spezifikation, Vektor Elemente in den Eigenschaften **headingproperties** und **titlesofparts** sollten an 32-Bit-Begrenzungen innerhalb des Eigenschaften Satzes ausgerichtet werden. In den Eigenschaften Sätzen **documentsummaryinformation** und **User Defined** müssen diese Elemente jedoch gepackt werden, wenn die Codepage des Eigenschaften Satzes nicht Unicode ist.

 

</dd> </dl>

Der **benutzerdefinierte** Eigenschaften Satz kann verwendet werden, um alle Eigenschaften zu speichern. In der Regel wird es verwendet, um benannte Eigenschaften zu speichern, die von einem Benutzer erstellt wurden.

 

 




