---
title: Kompilieren der mit dem SDK bereitgestellten IDL-Dateien
description: Kompilieren der mit dem SDK bereitgestellten IDL-Dateien
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Geräte-Manager,IDL-Dateien
- Geräte-Manager,IDL-Dateien
- Desktopanwendungen, IDL-Dateien
- Dienstanbieter, IDL-Dateien
- Programmierhandbuch, IDL-Dateien
- IDL-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444011"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Kompilieren der mit dem SDK bereitgestellten IDL-Dateien

Das Windows Media Geräte-Manager SDK enthält sowohl Headerdateien als auch die IDL-Quelldateien für die meisten dieser Headerdateien. Die Headerdateien befinden sich im \\ Ordner inc \\ im SDK-Installationspfad. Die IDL-Dateien befinden sich im \\ Ordner \\ idl.

Die vorkompilierten Header sind viel einfacher zu verwenden, und einige der IDL-Dateien werden zu einem einzelnen bereitgestellten Header kombiniert. Wenn Sie jedoch ihre eigenen Headerdateien aus den bereitgestellten IDL-Dateien verarbeiten möchten, wird in diesem Thema beschrieben, welche IDL-Dateien welche Headerdateien erstellen, und es werden auch die Abhängigkeiten der einzelnen IDL-Dateien beschrieben.

**Äquivalente IDL- und bereitgestellte Headerdateien**



| **Idl**                                                                                            | **Entsprechender angegebener Header**               | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM.idl<br/> WMSP.idl<br/> WMSCP.idl<br/> icomponentauthenticate.idl<br/> | Mswmdm.h                                     | Alle vier IDL-Dateien sind in diesem einzelnen bereitgestellten Header enthalten.<br/> **WMDM.idl** Definiert alle Anwendungsschnittstellen und erforderlichen Strukturen, Konstanten und Fehlercodes.<br/> **WMSP.idl** Definiert alle Dienstanbieterschnittstellen.<br/> **WMSCP.idl** Definiert alle Schnittstellen, GUID-Werte und Konstanten, die von sicheren Inhaltsanbietern benötigt werden.<br/> **icomponentauthenticate.idl** Definiert die [**IComponentAuthenticate-Schnittstelle.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)<br/> |
| Wmdmlog.idl                                                                                        | Wmdmlog.h<br/> wmdmlog \_ i.c<br/> | Definiert die Protokollierungsschnittstellen.<br/> Beide angegebenen Headerdateien müssen aufgrund eines Problems mit der IDL-Datei anstelle der H-Datei verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp.idl                                                                                 | Wmdrmdeviceapp.h                             | Definiert die [**IWMDRMDeviceApp-**](iwmdrmdeviceapp.md) und [**IWMDRMDeviceApp2-Schnittstellen,**](iwmdrmdeviceapp2.md) die von Anwendungen verwendet werden, die DRM auf Geräten aktualisieren, oder die Anzahl der Wiedergaben von Zählern auf Geräten.                                                                                                                                                                                                                                                                                                                 |



 

**IDL-Abhängigkeiten**

Einige der bereitgestellten IDL-Dateien verfügen über Buildabhängigkeiten. Wenn Sie die IDL-Dateien selbst kompilieren möchten, müssen Sie diese externen Abhängigkeiten in der in der folgenden Tabelle gezeigten Reihenfolge verarbeiten.



|   Idl                      |   Abhängigkeiten                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| icomponentauthenticate.idl | import "oaidl.idl";<br/> \#include "icomponentauthenticate.idl"<br/> |
| WMDM.idl                   | Keine externen Abhängigkeiten                                                         |
| WmdmLog.idl                | Keine externen Abhängigkeiten                                                         |
| WMDRMDeviceApp.idl         | Keine externen Abhängigkeiten                                                         |
| WMSCP.idl                  | \#include "WMDRMDeviceApp.idl"<br/> \#include "WMSP.idl"<br/>        |
| WMSP.idl                   | \#include "WMDM.idl"                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





