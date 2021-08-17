---
description: Mit Windows Vista hat sich die Elementstruktur Windows Image Acquisition (WIA) erheblich geändert.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Informationen zur IWiaItem2-Elementstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae342f5a85e61b6384604dae703881c6888e3e1cf8e61cc8a39a32ac77ad436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264428"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Informationen zur IWiaItem2-Elementstruktur

Mit Windows Vista hat sich die Elementstruktur Windows Image Acquisition (WIA) erheblich geändert. [**IWiaItem2-Elemente**](-wia-iwiaitem2.md) werden verwendet, um Geräteattribute und Gerätedaten darzustellen. Imageerstellungsanwendungen sehen ein WIA 2.0-Gerät (Windows Image Acquisition) als hierarchische Struktur von Elementen, wobei das Stammelement das Gerät selbst und die untergeordneten Elemente darstellen, die Elemente wie programmierbare Datenquellen, Bilder oder Ordner darstellen, die Bilder enthalten.

-   [Anwendungselemente](#application-items)
-   [Elementflags](#item-flags)
-   [Elementkategorien](#item-categories)
-   [Stammelement](#root-item)
-   [Datenelement](#data-item)
-   [Zugehörige Themen](#related-topics)

## <a name="application-items"></a>Anwendungselemente

Die WIA 2.0-Elementstruktur, die eine Anwendung sehen kann, ist von der Struktur getrennt, die von einem WIA 2.0-Minitreiber erstellt und verwaltet wird. Wenn ein Minitreiber eine Struktur erstellt, verwendet der WIA 2.0-Dienst diese WIA 2.0-Elementstruktur als Leitfaden, um eine Kopie der Struktur zu erstellen, die von Imageerstellungsanwendungen angezeigt werden kann. Elemente in der kopierten Struktur werden als *Anwendungselemente* bezeichnet. Elemente in der von einem Minitreiber erstellten Struktur werden als *Treiberelemente* bezeichnet.

Ein WIA-Element kann eine programmierbare Datenquelle für den Dokumentfeeder eines Scanners oder die auf diesem Gerät gespeicherten Daten darstellen. Ein WIA-Gerät sollte in einzelne Elemente unterteilt werden, die verschiedene von diesem Gerät erzeugte Daten beschreiben.

Beispielsweise kann ein WIA-Scanner, der sowohl Flatbedscans als auch Dokumentfeederscans unterstützt, in zwei untergeordnete Elemente unterteilt werden. Eine stellt die Flatbed-Scanfunktionalität und die andere die Überprüfungsfunktionalität des Dokumentfeeders dar.

Mehrere Bilder, die auf einem Flatbedscanner angeordnet und gleichzeitig gescannt werden, können in einem Ordner platziert werden. Mithilfe des Segmentierungsfilters ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) kann jedes Bild oder jede Unterregion dann als untergeordnetes Element des Ordners erstellt werden.

Die WIA-Struktur für ein Kameragerät, das Fotos ("Film") speichert, kann in Elemente unterteilt werden, die Ordner, Unterordner und Fotos darstellen.

## <a name="item-flags"></a>Elementflags

WIA-Elementflags helfen beim Klassifizieren des Inhalts oder des unterstützten Verhaltens eines bestimmten WIA-Elements. WIA-Elementflags sind in zwei Gruppen unterteilt.

1.  Elementstatusflags melden den aktuellen Status des WIA-Elements, z. B. [**WiaItemTypeDisconnected,**](-wia-wia-item-type-flags.md) **WiaItemTypeDeleted** usw.
2.  Elementdatendarstellung/Verwendungsflags melden die Daten, die das WIA-Element darstellt oder bei der Übertragung erzeugen kann. Beispielsweise ist [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) ein Datendarstellungsflag, das der Anwendung mitteilt, dass die dem aktuellen WIA-Element zugeordneten Daten Bilddaten sind und Bilddateneigenschaften aufweisen sollten. **WIA \_ IPA ITEM FLAGS ist ein \_ \_ Elementverwendungsflag,** das die Anwendung darüber informiert, dass das WIA-Element konfigurierbar ist und einem Satz vordefinierter Konfigurationsregeln folgt, die auf der [**WIA IPA ITEM \_ \_ \_ CATEGORY**](-wia-wiaitempropcommonitem.md) basieren, und dass die Konfiguration möglicherweise das Ergebnis für jede Datenübertragung ändern kann. (Weitere Informationen zu Kategoriedefinitionen finden Sie unter [Elementkategorien](#item-categories) von Elementkategorien.)

Die folgende Grafik zeigt ein Beispiel für eine WIA-Elementstruktur und die verschiedenen Flags, die jedem Element zugeordnet sein können.

![Beispiele für Elementflags für Elemente in einer Struktur](images/scannertree1.jpg)

## <a name="item-categories"></a>Elementkategorien

WIA-Elemente werden mithilfe der [**WIA \_ IPA ITEM \_ \_ CATEGORY-Eigenschaftswerte**](-wia-wiaitempropcommonitem.md) in Kategorien gruppiert. Diese Kategorien definieren, wie ein WIA-Element behandelt oder verwendet werden soll. Wenn das Element beispielsweise eine fertige Datei (WIA \_ CATEGORY \_ FINISHED \_ FILE) darstellt, sollte eine WIA-Anwendung davon ausgehen, dass die Daten statisch sind und sich auf dem Gerät befinden. Wenn das Element einen Feeder (WIA \_ CATEGORY \_ FEEDER) darstellt, sollte die Anwendung erwarten, dass es die erforderlichen Eigenschaften des Dokumentfeeders enthält und wie ein Dokumentfeeder funktioniert.

Die von WIA definierten Kategorien sind:

-   WIA \_ CATEGORY \_ AUTO
-   WIA \_ CATEGORY \_ FEEDER
-   WIA \_ CATEGORY \_ FILM
-   \_ \_ FERTIGE \_ WIA-KATEGORIEDATEI
-   WIA \_ CATEGORY \_ FLATBED

Beispielsweise können für das Flatbedelement eines Scanners die [**WIA \_ IPA ITEM \_ \_ FLAGS**](-wia-wiaitempropcommonitem.md) auf [**WiaItemTypeImage,**](-wia-wia-item-type-flags.md) **WiaItemTypeTransfer** und **WiaItemTypeProgrammableDataSource** und die **WIA IPA ITEM \_ \_ \_ CATEGORY-Eigenschaft** auf WIA CATEGORY FLATBED festgelegt \_ \_ sein.

Die folgende Tabelle zeigt die WIA-Kategoriegruppierung mit Elementflags und WIA-Elementen. Diese Tabelle enthält keine vollständige Liste der WIA-Elementflags, die von WIA definiert werden.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>WIA-Kategorie</th>
<th>Gültige WIA-Elementflags</th>
<th>WIA-Eigenschaftensatz</th>
<th>WIA-Elemente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></li>
</ul></td>
<td>Der Eigenschaftensatz enthält automatisch konfigurierte Scannereigenschaften.</td>
<td>Automatisches WIA-Element, das die automatisch konfigurierten Scaneinstellungen des Scanners darstellt.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Der Eigenschaftensatz enthält Eigenschaften des Feederscanner-Steuerelements (in der Regel bild- und dokumentspezifische Eigenschaften).</td>
<td>WIA Feeder-Elemente, einschließlich untergeordneter Elemente, die die Front- und Back-Seiten eines Dokuments darstellen.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Der Eigenschaftensatz umfasst Eigenschaften von Filmscanner-Steuerelementen (normalerweise bild- und dokumentspezifische Eigenschaften).</td>
<td>WIA-Filmelemente, einschließlich untergeordneter Elemente, die die einzelnen Scanframes darstellen.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
</ul></td>
<td>Die für dieses Element festgelegte Eigenschaft hängt vom gemeldeten Elementtyp ab. Beispielsweise sollte <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> einige Bildelementeigenschaften wie Bits pro Pixel usw. enthalten.</td>
<td>WIA-Speicherelemente, einschließlich untergeordneter Elemente, die fertige Dateiinhalte darstellen (Datendateien wie JPEG, HTML, TXT usw.).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>– kann vorhanden sein, wenn der Scanner die Überprüfung mit mehreren Elemente unterstützt.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>– kann vorhanden sein, wenn die Anwendung während einer Überprüfungssitzung mit mehreren Element ein WIA-Element generiert.</li>
</ul></td>
<td>Der Eigenschaftensatz enthält Eigenschaften des Flatbedscanner-Steuerelements (in der Regel bild- und dokumentspezifische Eigenschaften).</td>
<td>WIA-Flatbed-Elemente, einschließlich untergeordneter Elemente, die Bereiche darstellen, die auf dem Flatbed-Kennzeichen des Scanners gescannt werden.</td>
</tr>
</tbody>
</table>



 

Die folgende Grafik zeigt ein Beispiel für eine WIA-Elementstruktur und die verschiedenen Kategorien, die jedem Element zugeordnet werden können.

![Beispiele für Elementkategorien für Elemente in einer Struktur](images/scannertree2.jpg)

## <a name="root-item"></a>Stammelement

Ein WIA-Stammelement ist ein Ordnerelement, das mit den Flags [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) und **WiaItemTypeDevice** markiert ist, die das Gerät selbst darstellen. Sie enthält Geräteattribute wie Hersteller, Gerätename und Treiberattribute wie Treiberversion und BENUTZEROBERFLÄCHEN-Klassenbezeichner (USER Interface Class Identifier, CLSID). Imageerstellungsanwendungen rufen den Stamm zur WIA-Elementstruktur ab, indem sie die [**IWiaDevMgr2::CreateDevice-Methode**](-wia-iwiadevmgr2-createdevice.md) aufrufen. Die Anwendung verwendet das Stammelement, um Zugriff auf die einzelnen untergeordneten WIA-Elemente zu erhalten, indem sie die Struktur aufzählt (siehe [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>Datenelement

Jedes Element, das zum Übertragen von Daten verwendet werden kann, wird als Datenelement betrachtet. Dies schließt Elemente ein, die mit dem [**Flag WiaItemTypeProgrammableDataSource gekennzeichnet**](-wia-wia-item-type-flags.md) sind.

Ordnerelemente und Nichtordnerelemente können die Möglichkeit zum Übertragen von Daten verfügbar machen, indem sie mit dem [**WiaItemTypeTransfer-Flag markiert**](-wia-wia-item-type-flags.md) werden. Jedes Element, für das dieses Flag festgelegt ist, muss die folgenden WIA-Elementeigenschaften bereitstellen:

-   [**\_ \_ WIA-IPA-ZUGRIFFSRECHTE \_**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ WIA-IPA-ELEMENTGRÖßE \_**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ WIA-IPA-PUFFERGRÖßE \_**](-wia-wiaitempropcommonitem.md)
-   [**\_WIA-IPA-FORMAT \_**](-wia-wiaitempropcommonitem.md)
-   [**BEVORZUGTES \_ WIA-IPA-FORMAT \_ \_**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ TYMED**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ WIA-IPA-DATEINAMENERWEITERUNG \_**](-wia-wiaitempropcommonitem.md)

Programmierbare Datenquellenelemente, die mit dem [**WiaItemTypeTransfer-Flag**](-wia-wia-item-type-flags.md) gekennzeichnet sind, müssen auch den erforderlichen Eigenschaftensatz für das Datenelement enthalten.

WIA-Datenelemente können abhängig von den Flageinstellungen des Elements zusätzliche Eigenschaften aufweisen. Beispielsweise sollten WIA-Elemente, die mit dem [**WiaItemTypeImage-Flag**](-wia-wia-item-type-flags.md) gekennzeichnet sind, bildspezifische Informationseigenschaften wie [**WIA \_ IPA \_ DEPTH**](-wia-wiaitempropcommonitem.md) und **WIA \_ IPA \_ NUMBER OF LINES \_ \_ aufweisen.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)
</dt> <dt>

[**IWiaDevMgr2**](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



