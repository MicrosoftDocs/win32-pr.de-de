---
title: WFP-API
description: Die WFP-API (Windows Filtering Platform) ist in die folgenden Komponenten unterteilt.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106338700"
---
# <a name="wfp-api"></a>WFP-API

Die WFP-API (Windows Filtering Platform) ist in die folgenden Komponenten unterteilt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>BESCHREIBUNG</th>
<th>Headerdateien</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout-API</a> (f) $ {Remove} $<br />
</td>
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Datentypen</a> , die von Legenden verwendet werden. <strong>Hinweis</strong>  Diese Datentypen sind im Microsoft Windows Driver Development Kit (DDK) dokumentiert.<br/></td>
<td><dl> "f"<br />
"f"<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Funktionen</a> und <a href="/windows-hardware/drivers/ddi/_netvista/">Enumerationstypen</a> , die zum Implementieren von Legenden verwendet werden. <strong>Hinweis</strong>  Diese Funktionen und Enumerationstypen sind im DDK dokumentiert.<br/></td>
<td><dl> "f"<br />
"f"<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">IKE/AuthIP API (IKEEXT) $ {Remove} $<br />
</td>
<td><a href="fwp-enums.md">Enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> , die zum Verwalten von IKE-und AuthIP-Hauptmodusrichtlinien-und-Sicherheits Zuordnungen verwendet werden.</td>
<td><dl> iketypes. h<br />
iketypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ike-functions.md">Funktionen</a> zum Verwalten von IKE-und AuthIP mm-Richtlinien und-Sicherheits Zuordnungen.</td>
<td><dl> "f"<br />
"f"<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">IPSec-API (IPSec) $ {Remove} $<br />
</td>
<td><a href="fwp-enums.md">Enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> zum Verwalten von IPSec-Richtlinien und Sicherheits Zuordnungen.</td>
<td><dl> ipsectypes. h<br />
ipsectypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ipsec-functions.md">Funktionen</a> zum Verwalten von IPSec-Richtlinien und Sicherheits Zuordnungen.</td>
<td><dl> "f"<br />
"f"<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">Verwaltungs-API (f) $ {Remove} $<br />
</td>
<td><a href="fwp-enums.md">Enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> , die zum Verwalten der Filter-Engine verwendet werden.</td>
<td><dl> "f"-Typen<br />
"f"-Typen. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-mgmt-functions.md">Funktionen</a> , die zum Verwalten der Filter-Engine verwendet werden. Diese Funktionen werden verwendet, um die folgenden Aufgaben auszuführen:<br/>
<ul>
<li>Festlegen und Abfragen von Filtern, Anbietern und Callouts.</li>
<li>Rufen Sie IPSec-Statistiken ab.</li>
<li>Konfigurieren Sie die Windows-Filter Plattform.</li>
</ul></td>
<td><dl> "f"<br />
"f"<br />
</dl></td>

</tr>
<tr class="odd">
<td>Freigegebene API (f)</td>
<td>Grundlegende <a href="fwp-enums.md">enumerierte Typen</a> und <a href="fwp-structs.md">Strukturen</a> , die von der Windows-Filter Plattform gemeinsam genutzt werden</td>
<td><dl> "f"<br />
"wptypes. idl"<br />
</dl></td>
</tr>
</tbody>
</table>



 

Datentyp Namen sind Großbuchstaben und Unterstriche. Der Name beginnt immer mit einem Präfix, das seine Komponentengruppe identifiziert, z. b. [**fwpm \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Funktionsnamen sind gemischte Groß-und Kleinschreibung. Der Name beginnt immer mit einem Präfix, das seine Komponentengruppe identifiziert, z. b. [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

Die meisten Daten-und Funktionsnamen enden mit einer Versionsnummer. In der Header Datei "fwpvi. h" werden Versions unabhängige Daten-und Funktionsnamen der Version zugeordnet, die für die Verwendung mit einem bestimmten Betriebssystem geeignet ist. Weitere Informationen finden Sie unter [WFP-Version-Independent Namen und für bestimmte Versionen von Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Jede Komponente ist nicht eigenständig. Beispielsweise werden die IKE-Hauptmodus-Richtlinien (mm) in der IKEEXT-Komponente definiert, jedoch in einem Anbieter Kontext gespeichert und einem Filter zugeordnet, der beide in der fwpm-API-Komponente enthalten sind.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode und Kernel-Mode öffentliche Header Dateien

Die meisten WFP-Funktionen können entweder über den Benutzermodus oder den Kernel Modus aufgerufen werden. Allerdings geben benutzermodusfunktionen einen **DWORD** -Wert zurück, der einen Win32-Fehlercode darstellt, wohingegen Kernel Modus-Funktionen einen **NTSTATUS** -Wert zurückgeben, der einen NT-Statuscode darstellt. Folglich sind Funktionsnamen und Semantik zwischen dem Benutzermodus und dem Kernel Modus identisch, aber die Funktions Signaturen sind nicht. Hierfür sind separate Benutzermodus-und kernelmodusspezifische Header für die Funktionsprototypen erforderlich. Die Header Dateinamen im Benutzermodus enden mit "u", und der kernelmodusdateiname endet mit "k".

In der folgenden Tabelle werden die Win32-Header Dateien aufgelistet, die die WFP-Funktionen definieren.

| Headerdateien | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "f"      | Kernel Modus-Funktionsprototypen für die Komponenten "swpm", "IPSec" und "IKEEXT". Nur im DDK verfügbar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "f"      | Im Benutzermodus-Funktionsprototypen für die Komponenten "swpm", "IPSec" und "IKEEXT". Nur im Microsoft Windows Software Development Kit (SDK) verfügbar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| "f"      | Kernel Modus-Funktionsprototypen und enumerierte Typen für die fwps-Komponente. Nur im DDK verfügbar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| "f"      | Funktionsprototypen im Benutzermodus und enumerierte Typen für die fwps-Komponente. Nur in der Windows SDK verfügbar. **Hinweis**  Die Enumerationstypen des Benutzermodus-fwps sind identisch mit den Enumerationstypen für den Kernel Modus-fwps. Diese Typen werden daher nur im DDK dokumentiert.<br/> **Hinweis**  Die Prototypen von fwps-Funktionen im Benutzermodus sind identisch mit den Prototypen der fwps-Funktion im Kernelmodus, mit Ausnahme des Rückgabecodes. Fwps-Funktionen im Benutzermodus geben ein **DWORD** zurück, wohingegen fwps-Funktionen im Kernelmodus den **NTSTATUS** zurückgeben. Folglich sind diese Funktionen nur im DDK dokumentiert.<br/> |



 

Alle benutzermodusfunktionen werden aus fwpuclnt.dll exportiert. Alle kernelmodusfunktionen werden aus fwpkclnt.sys exportiert.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Datentypen für die Verwaltung ("f") und "Callout" ("f")

Die meisten Datentypen von Datentypen, die für Verwaltungsaufgaben verwendet werden, z. b. das Hinzufügen von Filtern oder Aufrufen einer Anwendung oder eines Treibers, verfügen über ein eigenes WPS-Pendant. Die fwps-Datentypen werden während der eigentlichen Filterung des Netzwerk Datenverkehrs im Kontext einer Legenden Routine für die Klassifizierung verwendet.

Zum Hinzufügen eines Filters zu einer bestimmten Filter-Engine-Ebene sollte der Programmierer z. b. einen fwpm-Typ verwenden, wie z `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . b.:. Um zu überprüfen, von welcher Ebene ein Aufruf aufgerufen wird, sollte der Programmierer den entsprechenden fwps-Typ verwenden: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Einige fwps-Gegenstücke zu fwpm-Datentypen erweitern die ursprünglichen fwpm-Datentypen. Um z. b. eine Filterbedingung auf vielen Filter-Engine-Ebenen hinzuzufügen, gibt der Programmierer `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` unabhängig von der Filter-Engine-Schicht an. Zum Ermitteln eines Filter Bedingungs Werts gibt der Programmierer einen ebenenspezifischen fwps-Typ an, z `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` . b.:.

Die Datentypen für die Datentypen sind in der Regel kleiner als ihre Gegenstücke. Die Bezeichner der [**swpm-Filterungs Schicht**](management-filtering-layer-identifiers-.md) sind z. b. **GUID** s (16 Bytes), wohingegen die Bezeichner der [SWPS-filterebenenids](/windows-hardware/drivers/network/management-filtering-layer-identifiers) **UInt16** (16 Bit) sind. Die geringere Größe für die Datentypen von Datentypen verbessert die Systemleistung, da ganzzahlige Vergleiche **GUID** -Vergleiche für echt Zeit Datenverkehr überwiegen. Außerdem wird der Kernel Speicher effizient verwendet, da die fwps-Typen alle im Kernel zum Verwalten der Filter verwendet werden, während die fwpm-Typen im Benutzermodus gespeichert werden, um die verschiedenen Ebenen zu verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WFP-API-Objektmodell](object-model.md)
</dt> <dt>

[WFP-API-Objekt Verwaltung](object-management.md)
</dt> </dl>

