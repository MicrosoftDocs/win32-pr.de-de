---
title: WFP-API
description: Die Windows-API (WFP) ist in die folgenden Komponenten unterteilt.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eadbb3fb6383999b2bb8ef14c99ecb8beab3f88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470147"
---
# <a name="wfp-api"></a>WFP-API

Die Windows-API (WFP) ist in die folgenden Komponenten unterteilt.




| Komponente | BESCHREIBUNG | Headerdateien | 
|-----------|-------------|--------------|
| <a href="/windows-hardware/drivers/ddi/_netvista/">Callout-API</a> (FWPS)${REMOVE}$<br /> | <a href="/windows-hardware/drivers/ddi/_netvista/">Datentypen,</a> die von Rückrufen verwendet werden. <strong>Hinweis:</strong>  Diese Datentypen sind im Microsoft Windows Driver Development Kit (DDK) dokumentiert.<br /> | <dl> fwpstypes.h<br />fwpstypes.idl<br /></dl> | 
| <a href="/windows-hardware/drivers/ddi/_netvista/">Funktionen</a> und <a href="/windows-hardware/drivers/ddi/_netvista/">aufzählte Typen, die zum</a> Implementieren von Rückrufen verwendet werden. <strong>Hinweis:</strong>  Diese Funktionen und aufzählten Typen sind im DDK dokumentiert.<br /> | <dl> fwpsu.h<br />fwpsk.h<br /></dl> | 
| IKE/AuthIP-API (IKEEXT)${REMOVE}$<br /> | <a href="fwp-enums.md">Enumerierte Typen und Strukturen,</a> die zum Verwalten von Richtlinien und Sicherheitszuordnungen im IKE- und AuthIP-Hauptmodus (MM) verwendet werden. <a href="fwp-structs.md"></a> | <dl> iketypes.h<br />iketypes.idl<br /></dl> | 
| <a href="fwp-ike-functions.md">Funktionen,</a> die zum Verwalten von IKE- und AuthIP MM-Richtlinien und Sicherheitszuordnungen verwendet werden. | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| IPsec-API (IPSEC)${REMOVE}$<br /> | <a href="fwp-enums.md">Aufzählen von Typen und Strukturen, die</a> <a href="fwp-structs.md">zum</a> Verwalten von IPsec-Richtlinien und Sicherheitszuordnungen verwendet werden. | <dl> ipsectypes.h<br />ipsectypes.idl<br /></dl> | 
| <a href="fwp-ipsec-functions.md">Funktionen,</a> die zum Verwalten von IPsec-Richtlinien und Sicherheitszuordnungen verwendet werden. | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| Verwaltungs-API (FWPM)${REMOVE}$<br /> | <a href="fwp-enums.md">Enumerierte Typen und Strukturen,</a> <a href="fwp-structs.md">die zum</a> Verwalten der Filter-Engine verwendet werden. | <dl> fwpmtypes.h<br />fwpmtypes.idl<br /></dl> | 
| <a href="fwp-mgmt-functions.md">Funktionen,</a> die zum Verwalten der Filter-Engine verwendet werden. Diese Funktionen werden verwendet, um die folgenden Aufgaben auszuführen:<br /><ul><li>Legen Sie Filter, Anbieter und Aufrufe fest, und fragen Sie sie ab.</li><li>Abrufen von IPsec-Statistiken.</li><li>Konfigurieren Sie die Windows Filterplattform.</li></ul> | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| Freigegebene API (FWP) | Grundlegende <a href="fwp-enums.md">enumerierte Typen und Strukturen,</a> <a href="fwp-structs.md">die</a> von der Windows Filterplattform gemeinsam genutzt werden. | <dl> fwptypes.h<br />fwptypes.idl<br /></dl> | 




 

Datentypnamen sind alle in Groß- und Unterstrichen getrennt. Der Name beginnt immer mit einem Präfix, das seine Komponentengruppe identifiziert, z. [**B. FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Funktionsnamen werden in gemischter Und-Case-Ung mit Trennzeichen verwendet. Der Name beginnt immer mit einem Präfix, das seine Komponentengruppe identifiziert, z. B. [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

Die meisten Daten- und Funktionsnamen enden mit einer Versionsnummer. Die Headerdatei fwpvi.h ordnet versionsunabhängige Daten und Funktionsnamen der Version zu, die für die Verwendung mit einem bestimmten Betriebssystem geeignet ist. Weitere Informationen finden Sie unter [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Jede Komponente ist nicht allein. Beispielsweise werden RICHTLINIEN für den IKE-Hauptmodus (MM) in der IKEEXT-Komponente definiert, aber in einem Anbieterkontext gespeichert und einem Filter zugeordnet, die beide in der FWPM-API-Komponente enthalten sind.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode und Kernel-Mode öffentliche Headerdateien

Die meisten WFP-Funktionen können entweder im Benutzermodus oder im Kernelmodus aufgerufen werden. Benutzermodusfunktionen geben jedoch einen **DWORD-Wert** zurück, der einen Win32-Fehlercode darstellt, während Kernelmodusfunktionen einen **NTSTATUS-Wert** zurückgeben, der einen NT-Statuscode darstellt. Daher sind Funktionsnamen und Semantik zwischen Benutzermodus und Kernelmodus identisch, Funktionssignaturen jedoch nicht. Dies erfordert separate benutzer- und kernelmodusspezifische Header für die Funktionsprototypen. Headerdateinamen im Benutzermodus enden auf "u", und Headerdateinamen im Kernelmodus enden auf "k".

In der folgenden Tabelle sind die Win32-Headerdateien aufgeführt, die die WFP-Funktionen definieren.

| Headerdateien | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk.h      | Funktionsprototypen im Kernelmodus für FWPM-, IPsec- und IKEEXT-Komponenten. Nur im DDK verfügbar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu.h      | Prototypen von Benutzermodusfunktionen für FWPM-, IPsec- und IKEEXT-Komponenten. Nur im Microsoft Windows Software Development Kit (SDK) verfügbar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk.h      | Prototypen von Kernelmodusfunktionen und aufzählte Typen für die FWPS-Komponente. Nur im DDK verfügbar.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu.h      | Prototypen von Funktionen im Benutzermodus und aufzählte Typen für die FWPS-Komponente. Nur im Windows SDK verfügbar. **Hinweis:**  Die aufzählten FWPS-Typen im Benutzermodus sind identisch mit den FWPS-enumerierten Typen im Kernelmodus. Daher sind diese Typen nur im DDK dokumentiert.<br/> **Hinweis:**  Die Prototypen der FWPS-Funktion im Benutzermodus sind mit den Prototypen der FWPS-Funktion im Kernelmodus identisch, mit Ausnahme des Rückgabecodes. FWPS-Funktionen im Benutzermodus geben **ein DWORD** zurück, während FWPS-Funktionen im Kernelmodus **ntstatus zurückgeben.** Daher sind diese Funktionen nur im DDK dokumentiert.<br/> |



 

Alle Benutzermodusfunktionen werden aus der fwpuclnt.dll. Alle Kernelmodusfunktionen werden aus fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Verwaltungsdatentypen (FWPM) und Callout-Datentypen (FWPS)

Die meisten FWPM-Datentypen, die für Verwaltungsaufgaben wie das Hinzufügen von Filtern oder Rückrufen aus einer Anwendung oder einem Treiber verwendet werden, verfügen über FWPS-Entsprechungen. Die FWPS-Datentypen werden während der tatsächlichen Filterung des Netzwerkdatenverkehrs im Kontext einer Calloutroutine für die Klassifizierung verwendet.

Um beispielsweise einer bestimmten Filtermodulebene einen Filter hinzuzufügen, sollte der Programmierer einen FWPM-Typ wie verwenden: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Um zu überprüfen, von welcher Ebene eine Callout aufgerufen wird, sollte der Programmierer den entsprechenden FWPS-Typ verwenden: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Einige FWPS-Entsprechungen zu FWPM-Datentypen erweitern die ursprünglichen FWPM-Datentypen. Um beispielsweise eine Filterbedingung auf vielen Filtermodulebenen hinzuzufügen, gibt der Programmierer unabhängig von der `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` Filtermodulebene an. Um einen Filterbedingungswert zu finden, gibt der Programmierer einen ebenenspezifischen FWPS-Typ an, z. B.: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

Die FWPS-Datentypen sind im Allgemeinen kleiner als ihre FWPM-Entsprechungen. Die Bezeichner der [**FWPM-Filterebene**](management-filtering-layer-identifiers-.md) sind z. B. **GUIDs**(16 Bytes), während die FWPS-Filterebenenbezeichner **UINT16** (16 Bits) sind. [](/windows-hardware/drivers/network/management-filtering-layer-identifiers) Die kleinere Größe für FWPS-Datentypen verbessert die Systemleistung, da ganzzahlige Vergleiche **GUID-Vergleiche** für Echtzeitdatenverkehr überwiegen. Außerdem wird der Kernelspeicher effizient verwendet, da alle FWPS-Typen im Kernel zum Verwalten der Filter verwendet werden, während die FWPM-Typen im Benutzermodus gespeichert werden, um die verschiedenen Ebenen zu verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WFP-API-Objektmodell](object-model.md)
</dt> <dt>

[WFP-API-Objektverwaltung](object-management.md)
</dt> </dl>

