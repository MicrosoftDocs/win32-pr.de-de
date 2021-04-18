---
title: Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden
description: Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Device Manager, IDL-Dateien
- Device Manager, IDL-Dateien
- Desktop Anwendungen, IDL-Dateien
- Dienstanbieter, IDL-Dateien
- Programmier Handbuch, IDL-Dateien
- IDL-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337998"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Kompilieren der IDL-Dateien, die mit dem SDK bereitgestellt werden

Das Windows Media Device Manager SDK umfasst sowohl Header Dateien als auch die Quell-IDL-Dateien für die meisten dieser Header Dateien. Die Header Dateien befinden sich im \\ Ordner "Inc" \\ im SDK-Installationspfad. Die IDL-Dateien befinden sich im \\ IDL- \\ Ordner.

Die vorkompilierten Header sind viel einfacher zu verwenden, und mehrere der IDL-Dateien werden zu einem einzelnen bereitgestellten Header zusammengefasst. Wenn Sie jedoch ihre eigenen Header Dateien aus den bereitgestellten IDL-Dateien verarbeiten möchten, wird in diesem Thema beschrieben, welche IDL-Dateien welche Header Dateien erstellen. Außerdem werden die Abhängigkeiten der einzelnen IDL-Dateien beschrieben.

**Äquivalente IDL und bereitgestellte Header Dateien**



| **IDL**                                                                                            | **Gleichwertig bereitgestellter**               | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM. idl<br/> Wmsp. idl<br/> Wmscp. idl<br/> icomponentauthenticate. idl<br/> | Mtaumdm. h                                     | Alle vier IDL-Dateien sind in diesem einzelnen bereitgestellten Header enthalten.<br/> **WMDM. idl** definiert alle Anwendungsschnittstellen und erforderlichen Strukturen, Konstanten und Fehlercodes.<br/> **Wmsp. idl** definiert alle Dienstanbieter Schnittstellen.<br/> **Wmscp. idl** definiert alle Schnittstellen, GUID-Werte und Konstanten, die von sicheren Inhaltsanbietern benötigt werden.<br/> **icomponentauthenticate. idl** definiert die [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle.<br/> |
| Wmdmlog. idl                                                                                        | Wmdmlog. h<br/> wmdmlog \_ i. c<br/> | Definiert die Protokollierungs Schnittstellen.<br/> Beide bereitgestellten Header Dateien müssen anstelle der h-Datei verwendet werden, da ein Problem mit der IDL-Datei vorliegt.<br/>                                                                                                                                                                                                                                                                                                                                                |
| Wmdrmdeviceapp. idl                                                                                 | Wmdrmdeviceapp. h                             | Definiert die [**iwmdrmdeviceapp**](iwmdrmdeviceapp.md) -und [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) -Schnittstellen, die von Anwendungen verwendet werden, die DRM auf Geräten oder die Anzahl der Wiedergabe Zähler auf Geräten aktualisieren.                                                                                                                                                                                                                                                                                                                 |



 

**IDL-Abhängigkeiten**

Einige der bereitgestellten IDL-Dateien haben Buildabhängigkeiten. Wenn Sie beabsichtigen, die IDL-Dateien selbst zu kompilieren, müssen Sie diese externen Abhängigkeiten in der in der folgenden Tabelle gezeigten Reihenfolge verarbeiten.



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| **IDL**                    | **Abhängigkeiten**                                                                 |
| icomponentauthenticate. idl | Importieren Sie "oaidl. idl";<br/> \#"icomponentauthenticate. idl" einschließen<br/> |
| WMDM. idl                   | Keine externen Abhängigkeiten                                                         |
| Wmdmlog. idl                | Keine externen Abhängigkeiten                                                         |
| Wmdrmdeviceapp. idl         | Keine externen Abhängigkeiten                                                         |
| Wmscp. idl                  | \#"wmdrmdeviceapp. idl" einschließen<br/> \#"wmsp. idl" einschließen<br/>        |
| Wmsp. idl                   | \#"WMDM. idl" einschließen                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





