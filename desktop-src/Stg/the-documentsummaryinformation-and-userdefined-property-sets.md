---
title: Die DocumentSummaryInformation- und UserDefined-Eigenschaftensätze
description: Ein DocumentSummaryInformation- und UserDefined-Eigenschaftensatz ist eine Erweiterung des Eigenschaftensatzes Zusammenfassungsinformationen. Beide Eigenschaftensätze können gleichzeitig vorhanden sein.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- UserDefined-Eigenschaftensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d76c679fd8b4059e821598bed37d68735c45f914e4685e43a1c514b832e199e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886836"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Die DocumentSummaryInformation- und UserDefined-Eigenschaftensätze

Ein **DocumentSummaryInformation-** und **UserDefined-Eigenschaftensatz** ist eine Erweiterung [des Eigenschaftensatzes Zusammenfassungsinformationen.](the-summary-information-property-set.md) Beide Eigenschaftensätze können gleichzeitig vorhanden sein.

Der Name des Streams, der den **DocumentSummaryInformation-Eigenschaftensatz** enthält, ist **\\ "005DocumentSummaryInformation".** Der Formatbezeichner (FMTID) für den **DocumentSummaryInformation-Eigenschaftensatz** ist **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

Die Deklaration für diesen Wert ist in den bereitgestellten Headerdateien als **FMTID \_ DocSummaryInformation** verfügbar. Weitere Informationen finden Sie unter [Namen in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) und [Format Identifiers](format-identifiers.md).

Dieser Stream verfügt auch über einen separaten Abschnitt für die benutzerdefinierten Eigenschaften wie in den **Eigenschaftensätzen DocumentSummaryInformation** und **UserDefined.** Dieser Abschnitt wird in der [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) als separater Eigenschaftensatz mit dem folgenden FMTID (verfügbar als **FMTID \_ UserDefinedProperties)** angezeigt: **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Diese beiden Eigenschaftensätze sind die einzigen, für die ein einzelner Stream mehrere Eigenschaftensätze enthalten kann. Die Tatsache, dass sich diese beiden Eigenschaftensätze in einem einzelnen Stream befinden, wirkt sich auf das Verhalten der **IPropertySetStorage-Schnittstelle** aus. Weitere Informationen finden Sie unter [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

In der folgenden Tabelle sind die eigenschaften aufgeführt, die dem **DocumentSummaryInformation-** und **UserDefined-Eigenschaftensatz** hinzugefügt wurden. Wie beim **SummaryInformation-Eigenschaftensatz** werden die Namen in der Regel nicht im Eigenschaftensatz gespeichert, sondern aus dem Eigenschaftenbezeichner abgeleitet.



| Eigenschaftenname      | Eigenschaftsbezeichner     | Eigenschaftsbezeichnerwert | VARIANT-Typ                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Kategorie           | **PIDDSI \_ CATEGORY**    | 0x00000002                | **VT \_ LPSTR**                     |
| PresentationTarget | **PIDDSI \_ PRESFORMAT**  | 0x00000003                | **VT \_ LPSTR**                     |
| Byte              | **PIDDSI \_ BYTECOUNT**   | 0x00000004                | **VT \_ I4**                        |
| Linien              | **PIDDSI \_ LINECOUNT**   | 0x00000005                | **VT \_ I4**                        |
| Absätze         | **PIDDSI \_ PARCOUNT**    | 0x00000006                | **VT \_ I4**                        |
| Folien             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **VT \_ I4**                        |
| Hinweise              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **VT \_ I4**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **VT \_ I4**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | 0x0000000A                | **VT \_ I4**                        |
| ScaleCrop          | **PIDDSI \_ SCALE**       | 0x0000000B                | **VT \_ BOOL**                      |
| HeadingPairs       | **PIDDSI \_ HEADINGPAIR** | 0x0000000C                | **VT \_ VARIANT** \| **VT \_ VECTOR** |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_ VECTOR** \| **VT \_ LPSTR**   |
| Manager            | **PIDDSI \_ MANAGER**     | 0x0000000E                | **VT \_ LPSTR**                     |
| Company            | **PIDDSI \_ COMPANY**     | 0x0000000F                | **VT \_ LPSTR**                     |
| LinksUpToDate      | **PIDDSI \_ LINKSDIRTY**  | 0x00000010                | **VT \_ BOOL**                      |



 

Diese Eigenschaften werden wie folgt verwendet:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie
</dt> <dd>

Eine vom Benutzer eingegebene Textzeichenfolge, die angibt, zu welcher Kategorie die Datei gehört (Memo, Vorschlag usw.). Dies ist nützlich, um Dateien desselben Typs zu suchen.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Zielformat für die Präsentation (35mm, Drucker, Video usw.).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes
</dt> <dd>

Die Anzahl von Bytes.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Linien
</dt> <dd>

Anzahl der Zeilen.

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Absätze
</dt> <dd>

Anzahl der Absätze.

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Folien
</dt> <dd>

Anzahl der Folien.

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notizen
</dt> <dd>

Anzahl der Seiten, die Notizen enthalten.

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides
</dt> <dd>

Anzahl der ausgeblendeten Folien.

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips
</dt> <dd>

Anzahl von Sound- oder Videoclips.

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop
</dt> <dd>

Legen Sie auf True (-1) fest, wenn die Skalierung der Miniaturansicht gewünscht ist. Wenn nicht festgelegt, ist das Zuschneiden erwünscht.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

Intern verwendete Eigenschaft, die die Gruppierung verschiedener Dokumentteile und die Anzahl der Elemente in jeder Gruppe angibt. Die Titel der Dokumentteile werden in der **TitlesofParts-Eigenschaft** gespeichert. Die **HeadingPairs-Eigenschaft** wird als Vektor von Varianten in sich wiederholenden Paaren von **VT \_ LPSTR-Werten** (oder **VT \_ LPWSTR**) und **VT \_ I4-Werten** gespeichert. Der **VT \_ LPSTR-Wert** stellt einen Überschriftennamen dar, und der **VT \_ I4-Wert** gibt die Anzahl der Dokumentteile unter dieser Überschrift an.

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts
</dt> <dd>

Namen von Dokumentteilen.

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager
</dt> <dd>

Manager des Projekts.

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Unternehmen
</dt> <dd>

Firmenname.

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate
</dt> <dd>

Boolescher Wert, um anzugeben, ob die benutzerdefinierten Links für alle Anwendungen durch übermäßiges Rauschen beeinträchtigt werden.

> [!Note]  
> Wie in 12.3 beschrieben. Serialisiertes Format für Eigenschaftensätze der OLE 2.0-Entwurfsspezifikation, Vektorelemente in den **Eigenschaften HeadingPairs** und **TitlesofParts** sollten an 32-Bit-Grenzen innerhalb des Eigenschaftensets ausgerichtet werden. Wenn die Codepage des Eigenschaftensets jedoch nicht Unicode ist, müssen diese Elemente in den **Eigenschaftensätzen DocumentSummaryInformation** und **UserDefined** gepackt werden.

 

</dd> </dl>

Der **UserDefined-Eigenschaftensatz** kann verwendet werden, um beliebige Eigenschaften zu enthalten. In der Regel wird es verwendet, um benannte Eigenschaften zu speichern, die von einem Benutzer erstellt wurden.

 

 




