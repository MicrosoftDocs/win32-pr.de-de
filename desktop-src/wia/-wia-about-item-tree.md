---
description: Bei Windows Vista wurde die Elementstruktur der Windows-Abbild Beschaffung (WIA) erheblich geändert.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Informationen zur IWiaItem2-Elementstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865256"
---
# <a name="about-the-iwiaitem2-item-tree"></a>Informationen zur IWiaItem2-Elementstruktur

Bei Windows Vista wurde die Elementstruktur der Windows-Abbild Beschaffung (WIA) erheblich geändert. [**IWiaItem2**](-wia-iwiaitem2.md) Items werden verwendet, um Geräte Attribute und Gerätedaten darzustellen. Abbild Erstellungs Anwendungen sehen ein Windows-Abbild Erfassungsgerät (WIA) 2,0 als hierarchische Struktur von Elementen, wobei das Stamm Element das eigentliche Gerät und die untergeordneten Elemente darstellt, die Elemente wie programmierbare Datenquellen, Bilder oder Ordner darstellen, die Bilder enthalten.

-   [Anwendungs Elemente](#application-items)
-   [Elementflags](#item-flags)
-   [Element Kategorien](#item-categories)
-   [Stamm Element](#root-item)
-   [Datenelement](#data-item)
-   [Zugehörige Themen](#related-topics)

## <a name="application-items"></a>Anwendungs Elemente

Die WIA 2,0-Elementstruktur, die eine Anwendung sehen kann, ist getrennt von der Struktur, die von einem WIA 2,0 Minidriver erstellt und verwaltet wird. Wenn ein Mini Treiber eine Struktur erstellt, verwendet der WIA 2,0-Dienst diese WIA 2,0-Elementstruktur als Leitfaden, um eine Kopie der Struktur zu erstellen, die von Abbild Erstellungs Anwendungen angezeigt werden kann. Elemente in der kopierten Struktur werden als *Anwendungs* Elemente bezeichnet. Elemente in der Struktur, die von einem Mini Treiber erstellt werden, werden als *Treiber* Elemente bezeichnet.

Ein WIA-Element kann eine programmierbare Datenquelle für die Dokument-oder Daten eines Scanners darstellen, die auf diesem Gerät gespeichert sind. Ein WIA-Gerät sollte in einzelne Elemente unterteilt werden, die verschiedene Daten beschreiben, die von diesem Gerät erzeugt werden.

Beispielsweise kann ein WIA-Scanner, der sowohl die Überprüfung des Flatbed als auch das Scannen von Dokumenten Scans unterstützt, unterteilt werden. Eine stellt die Überprüfungs Funktion für Flat-Scans dar, und die andere stellt die Scanfunktion für die Dokument Prüfung dar.

Mehrere Abbilder, die auf einem flachen Scanner angeordnet und gleichzeitig gescannt werden, können in einem einzigen Ordner abgelegt werden. Mithilfe des Segmentierungs Filters ([**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md)) kann jedes Bild oder jede Unterregion als untergeordnetes Element des Ordners erstellt werden.

Die WIA-Struktur für ein Kamera Gerät, das Fotos speichert ("Film"), kann in Elemente aufgeteilt werden, die Ordner, Unterordner und Fotos darstellen.

## <a name="item-flags"></a>Elementflags

WIA-elementflags helfen, den Inhalt oder das unterstützte Verhalten eines bestimmten WIA-Elements zu klassifizieren. WIA-elementflags fallen in zwei Gruppen.

1.  Elementstatusflags melden den aktuellen Status des WIA-Elements, z. b. [**wiaitemtypegetrennte**](-wia-wia-item-type-flags.md), **wiaitemtypedeleted** usw.
2.  Elementdaten Darstellung/nutzungsflags melden die Daten, die das WIA-Element darstellt oder bei der Übertragung erzeugt. [**Wiaitemtypeimage**](-wia-wia-item-type-flags.md) ist beispielsweise ein Daten Darstellungs Flag, das der Anwendung mitteilt, dass die Daten, die dem aktuellen WIA-Element zugeordnet sind, Bilddaten sind und über Bild Daten Eigenschaften verfügen sollen. **WIA \_ IPA \_ - \_ elementflags** ist ein Element für die Element Verwendung, das der Anwendung mitteilt, dass das WIA-Element konfigurierbar ist und einem Satz vordefinierter Konfigurations Regeln entsprechend der [**WIA \_ IPA- \_ Element \_ Kategorie**](-wia-wiaitempropcommonitem.md) folgt und dass die Konfiguration das Ergebnis für jede Datenübertragung möglicherweise ändern kann. (Weitere Informationen zu Kategoriedefinitionen finden [Sie Unterelement Kategorien](#item-categories) Element Kategorien.)

Die folgende Abbildung zeigt ein Beispiel für eine WIA-Elementstruktur und die verschiedenen Flags, die jedem Element zugeordnet werden können.

![Beispiele für elementflags für Elemente in einer Struktur](images/scannertree1.jpg)

## <a name="item-categories"></a>Element Kategorien

WIA-Elemente werden mithilfe der [**WIA \_ IPA \_ Element \_ Category**](-wia-wiaitempropcommonitem.md) -Eigenschaftswerte in Kategorien gruppiert. Diese Kategorien definieren, wie ein WIA-Element behandelt oder verwendet werden soll. Wenn das Element z. b. eine fertige Datei (die \_ Datei mit der Kategorie ist \_ abgeschlossen \_ ) darstellt, sollte eine WIA-Anwendung davon ausgehen, dass die Daten statisch sind und sich auf dem Gerät befinden. Wenn das Element einen feedvorgang (WIA \_ Category \_ Feeder) darstellt, sollte die Anwendung erwarten, dass Sie die erforderlichen Eigenschaften für die Dokument feederstellung enthält und wie eine Dokument-feederstellung funktioniert.

Die von WIA definierten Kategorien lauten:

-   Automatische WIA- \_ Kategorie \_
-   Kategorie- \_ \_ Feeder WIA
-   Film der Kategorie "WIA" \_ \_
-   Datei der WIA- \_ Kategorie \_ abgeschlossen \_
-   WIA- \_ Kategorie \_

Beispielsweise kann für das Element des Typs für einen Scanner die [**WIA \_ IPA \_ - \_ elementflags**](-wia-wiaitempropcommonitem.md) auf [**wiaitemtypeimage**](-wia-wia-item-type-flags.md), **wiaitemtypetransfer** und **wiaitemtypeprogrammiabledatasource** festgelegt werden, und die **WIA \_ IPA \_ Item \_ Category** -Eigenschaft ist auf die WIA-Kategorie "vereinfacht" festgelegt \_ \_ .

Die folgende Tabelle zeigt die WIA-kategoriengruppierung mit elementflags und WIA-Elementen. Diese Tabelle enthält keine vollständige Liste der WIA-elementflags, die von WIA definiert werden.



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
<th>Gültige WIA-elementflags</th>
<th>WIA-Eigenschaften Satz</th>
<th>WIA-Elemente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefile</strong></a></li>
</ul></td>
<td>Der Eigenschaften Satz umfasst automatisch konfigurierte Scanner-Eigenschaften.</td>
<td>Ein automatisches Element, das die automatisch konfigurierten Überprüfungs Einstellungen des Scanners darstellt.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypedocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a></li>
</ul></td>
<td>Der Eigenschaften Satz umfasst Eigenschaften des feedscannersteuerelements (normalerweise Bild-und Dokument spezifischer Eigenschaften Satz).</td>
<td>WIA-feeselemente, einschließlich untergeordneter Elemente, die die Vorder-und Hintergrund Seiten eines Dokuments darstellen.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a></li>
</ul></td>
<td>Der Eigenschaften Satz umfasst die Eigenschaften für den Filmscanner-Steuerelement (normalerweise Bild-und Dokument spezifischer Eigenschaften Satz)</td>
<td>WIA-Film Elemente, einschließlich untergeordneter Elemente, die die einzelnen scanungs Rahmen darstellen.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeaudiodatei</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypevideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypedocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></li>
</ul></td>
<td>Die für dieses Element festgelegte Eigenschaft hängt vom Typ des gemeldeten Elements ab. Beispielsweise sollte <a href="-wia-wia-item-type-flags.md"><strong>wiaitemtypeimage</strong></a> einige Bildelement Eigenschaften wie Bits pro Pixel usw. enthalten.</td>
<td>WIA-Speicherelemente, einschließlich untergeordneter Elemente, die den fertiggestellten Dateiinhalt darstellen (Datendateien wie JPEG, HTML, txt usw.).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypedocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a>– kann vorhanden sein, wenn der Scanner das Scannen von mehreren Elementen unterstützt.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypegenerated</strong></a>– kann vorhanden sein, wenn die Anwendung während einer Scan Sitzung mit mehreren Elementen ein WIA-Element generiert.</li>
</ul></td>
<td>Der Eigenschaften Satz umfasst Eigenschaften für das Überprüfung des über prüfbilds (normalerweise Bild-und Dokument spezifischer Eigenschaften Satz).</td>
<td>Elemente mit einem flachen Element, einschließlich untergeordneter Elemente, die Bereiche darstellen, die auf der Registerkarte "Flatbed" des Scanners gescannt werden.</td>
</tr>
</tbody>
</table>



 

Die folgende Abbildung zeigt ein Beispiel für eine WIA-Elementstruktur und die verschiedenen Kategorien, die jedem Element zugeordnet werden können.

![Beispiele für Element Kategorien für Elemente in einem Baum](images/scannertree2.jpg)

## <a name="root-item"></a>Stamm Element

Ein WIA-Stamm Element ist ein Ordner Element, das mit [**wiaitemtyperoot**](-wia-wia-item-type-flags.md) -und **wiaitemtypedevice** -Flags gekennzeichnet ist, die das Gerät selbst darstellen. Sie enthält Geräte Attribute wie Hersteller, Gerätename und Treiber Attribute wie Treiber Version und Benutzeroberflächen-Klassen Bezeichner (CLSID). Abbild Erstellungs Anwendungen rufen den Stamm der WIA-Elementstruktur auf, indem Sie die [**IWiaDevMgr2:: createdevice**](-wia-iwiadevmgr2-createdevice.md) -Methode aufrufen. Die Anwendung verwendet das root-Element, um Zugriff auf die einzelnen untergeordneten WIA-Elemente zu erhalten, indem die Struktur aufgelistet wird (siehe [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>Datenelement

Alle Elemente, die zum Übertragen von Daten verwendet werden können, werden als Datenelement betrachtet. Dies schließt Elemente ein, die mit dem [**wiaitemtypeprogrammiabledatasource**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet sind.

Ordner Elemente und nicht Ordner Elemente können die Möglichkeit zur Übertragung von Daten verfügbar machen, indem Sie mit dem [**wiaitemtypetransfer**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet werden. Jedes Element, für das dieses Flag festgelegt ist, muss die folgenden WIA-Element Eigenschaften bereitstellen:

-   [**WIA \_ IPA- \_ Zugriffs \_ Rechte**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA- \_ Element \_ Größe**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA- \_ Puffer \_ Größe**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA- \_ Format**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA- \_ bevorzugtes \_ Format**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ TYMED**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA- \_ Dateinamen \_ Erweiterung**](-wia-wiaitempropcommonitem.md)

Programmierbare Datenquellen Elemente, die mit dem [**wiaitemtypetransfer**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet sind, müssen außerdem die erforderliche Eigenschaft für das Datenelement angeben.

WIA-Datenelemente haben möglicherweise zusätzliche Eigenschaften, abhängig von den Flag-Einstellungen des Elements. Beispielsweise sollten WIA-Elemente, die mit dem [**wiaitemtypeimage**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet sind, über Bild spezifische Informations Eigenschaften verfügen, wie [**WIA \_ IPA- \_ Tiefe**](-wia-wiaitempropcommonitem.md) und **WIA \_ IPA- \_ Anzahl \_ von \_ Zeilen**.

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

 

 



