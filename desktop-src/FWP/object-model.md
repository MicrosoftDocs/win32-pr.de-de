---
title: Objektmodell
description: In der folgenden Tabelle sind die Objekttypen aufgelistet, die durch die verschiedenen von der Windows-Filter Plattform (WFP) bereitgestellten API-Sätze bearbeitet werden können.
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038600"
---
# <a name="object-model"></a>Objektmodell

In der folgenden Tabelle sind die Objekttypen aufgelistet, die durch die verschiedenen von der Windows-Filter Plattform (WFP) bereitgestellten API-Sätze bearbeitet werden können.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttyp</th>
<th>BESCHREIBUNG</th>
<th>Beispiel Eigenschaften</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Filter</td>
<td>Eine Regel, die die Klassifizierung regelt. Wenn die Bedingungen erfüllt sind, wird die Aktion aufgerufen. <br/> Dies ist das komplexeste Objekt, das von WFP verfügbar gemacht wird, da alle anderen Objekttypen miteinander verknüpft sind. <br/></td>
<td><ul>
<li>Array von Bedingungen</li>
<li>Aktion (zulassen, blockieren, Legenden)</li>
<li><a href="filter-weight-assignment.md">Weight</a></li>
<li>Kontext</li>
</ul></td>
<td>&quot;Blockieren Sie den Datenverkehr mit einem TCP-Port größer als 1024.&quot; <br/> &quot;Gibt für den gesamten Datenverkehr, der nicht gesichert ist, IDs an.&quot;<br/></td>
</tr>
<tr class="even">
<td>Legende</td>
<td>Eine Reihe von Funktionen, die am Klassifizierungsprozess teilnehmen.<br/> Dadurch kann die benutzerdefinierte Paketverarbeitung ausgeführt werden, wenn bestimmte Bedingungen erfüllt sind.<br/></td>
<td><ul>
<li>id</li>
<li>Anwendbare Ebene</li>
</ul></td>
<td>Der NAT-Treiber<br/></td>
</tr>
<tr class="odd">
<td>Ebene</td>
<td>Ein Filter Container in der Filter-Engine. <br/> Stellt einen bestimmten Punkt in der Verarbeitung des Netzwerk Datenverkehrs dar, bei dem die Filter-Engine aufgerufen wird.<br/></td>
<td><ul>
<li>Schema für Filter, die der Ebene hinzugefügt werden können</li>
</ul></td>
<td>Die eingehende Transport Schicht<br/></td>
</tr>
<tr class="even">
<td>Unterebene</td>
<td>Eine untergeordnete Komponente einer Ebene, die bei der <a href="filter-arbitration.md">Filterung von Filtern</a>verwendet wird.<br/></td>
<td><ul>
<li>Weight</li>
</ul></td>
<td>Die IPSec-Tunnel Unterschicht<br/></td>
</tr>
<tr class="odd">
<td>Anbieter</td>
<td>Ein Richtlinien Anbieter, der eine Lösung auf WFP erstellt hat.<br/> Sie wird ausschließlich zur Verwaltung verwendet. Sie wirkt sich nicht auf die Lauf Zeit Paketverarbeitung aus.<br/></td>
<td><ul>
<li>id</li>
<li>Dienstname</li>
</ul></td>
<td>Windows-Firewall mit erweiterter Sicherheit<br/> Eine Drittanbieter-URL-Filterungs Anwendung<br/></td>
</tr>
<tr class="even">
<td>Anbieter Kontext</td>
<td>Ein Daten-BLOB, das von einem Richtlinien Anbieter zum Speichern beliebiger Kontextinformationen verwendet wird. <br/> Es wird verwendet, um benutzerdefinierte Konfigurationsinformationen an eine Legende zu übergeben.<br/> Die gängigste Methode, die Kontextinformationen zu verwenden, besteht darin, dass Filter auf einen Anbieter Kontext verweisen. <br/></td>
<td><ul>
<li>id</li>
<li>Datenblob</li>
</ul></td>
<td>IPSec speichert Authentifizierungs Einstellungen in der Basis Filter-Engine (BFE). Die &quot; Kontext &quot; Eigenschaft eines Filters gibt die Authentifizierungs Einstellungen an, die für den Datenverkehr verwendet werden sollen, der vom Filter beschrieben wird.<br/> Der SSL-zertifizierungsauswahl-Shim speichert Zertifizierungs Informationen in einem Anbieter Kontext. <br/></td>
</tr>
</tbody>
</table>



 

Die von der WFP-API verfügbar gemachten Objekttypen haben eine konsistente Semantik. Die Aktionen von Add, Enumerate, subscribe usw. sind für alle Objekttypen ähnlich.

Jeder Objekttyp wird durch eine Datenstruktur dargestellt (z. b. " [**f \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)"). Um die Anzahl der unterschiedlichen Datenstrukturen zu minimieren, die von der WFP-API verfügbar gemacht werden, wird die gleiche Datenstruktur sowohl für das Hinzufügen neuer Objekte als auch für das Abrufen vorhandener Objekte verwendet. Daher können in jeder Datenstruktur Felder vorhanden sein, die beim Hinzufügen eines neuen Objekts ignoriert werden, da diese Felder von der Basis Filter-Engine (BFE) und nicht vom Aufrufer ausgefüllt werden. Beispielsweise verfügt eine **\_ FILTER0** -Datenstruktur vom Typ " **filterid** " über ein Feld "filterid", das die **LUID** der entsprechenden "f"- **\_ FILTER0** enthält. Diese **LUID** wird von BFE zugewiesen, und dieses Feld wird daher im [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)-Aufrufe ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objekt Verwaltung](object-management.md)
</dt> </dl>

 

 





