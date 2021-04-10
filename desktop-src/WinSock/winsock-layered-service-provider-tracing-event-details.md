---
description: Details zur Änderung der Winsock-Katalog Änderung
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Details zur Änderung der Winsock-Katalog Änderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130404"
---
# <a name="winsock-catalog-change-tracing-details"></a>Details zur Änderung der Winsock-Katalog Änderung

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Die Änderungs Ereignis Ablauf Verfolgung von Winsock-Katalogen für Schicht-Dienstanbieter (LSPs) bezieht sich auf die LSP-Installation, LSP-Entfernung, LSP-Deaktivierung und Winsock-Katalog Zurücksetzungs Vorgänge. Alle der folgenden Ereignisse werden in den Channel *Microsoft-Windows-Winsock-WS2HELP/Operational* geschrieben, der sich von der anderen in Windows Vista und höher angemeldeten Winsock-Netzwerk Ereignis Ablauf Verfolgung unterscheidet.

Im folgenden werden die einzelnen Winsock-LSP-Ereignisse aufgeführt, die verfolgt werden können, und es wird beschrieben, welche Parameter und Informationen protokolliert werden.

## <a name="lsp-install"></a>LSP-Installation

Ereignis-ID = 1

Ebene = 4 (Informationen)

Die folgenden Winsock-LSP-Ereignisse werden bei einem LSP-Installationsvorgang nachverfolgt:

-   Ein Protokolleintrag wird im Winsock-Katalog installiert.

Die folgenden Parameter werden für ein LSP-Installations Ereignis protokolliert:



| Parameter                                                                                                | BESCHREIBUNG                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name<br/>     | Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den installierten LSP abgerufen wird.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren<br/>         | Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP installiert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Ations<br/> | Der Modul Dateiname der Anwendung, die die LSP-Installation aufruft.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Der GUID-Wert des Winsock-Transport Anbieters, unter dem der LSP installiert wird.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie<br/>     | Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das zu installierende LSP.<br/>                                |



 

## <a name="lsp-uninstall"></a>LSP deinstallieren

Ereignis-ID = 2

Ebene = 4 (Informationen)

Die folgenden Winsock-LSP-Ereignisse werden bei einem LSP-Deinstallations Vorgang nachverfolgt:

-   Ein Protokolleintrag wird aus dem Winsock-Katalog entfernt.

Die folgenden Parameter werden für ein LSP-Deinstallations Ereignis protokolliert:



| Parameter                                                                                                | BESCHREIBUNG                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name<br/>     | Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den zu entfernenden LSP abgerufen wird.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren<br/>         | Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP entfernt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Ations<br/> | Der Modul Dateiname der Anwendung, die den LSP-Befehl zum Entfernen aufruft.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Der GUID-Wert des Winsock-Transport Anbieters, aus dem der LSP entfernt wird.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie<br/>     | Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für den LSP, der entfernt wird.<br/>                                |



 

## <a name="lsp-disable"></a>LSP deaktivieren

Ereignis-ID = 3

Ebene = 4 (Informationen)

Die folgenden Winsock-LSP-Ereignisse werden für einen LSP-Deaktivierungs Vorgang nachverfolgt:

-   Ein Protokolleintrag ist im Winsock-Katalog deaktiviert.

Die folgenden Parameter werden für ein LSP-Deaktivierungs Ereignis protokolliert:



| Parameter                                                                                                | BESCHREIBUNG                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name<br/>     | Der Name des LSP, der vom **szprotocol** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP abgerufen wird.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren<br/>         | Der Winsock-Katalog (32 Bit oder 64 Bit), in dem der LSP deaktiviert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Ations<br/> | Der Modul Dateiname der Anwendung, die die LSP-Deaktivierung aufruft.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Der GUID-Wert des Winsock-Transport Anbieters, bei dem der LSP deaktiviert wird.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie<br/>     | Der **dwcatalogentryid** -Member der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur für das deaktivierte LSP.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Winsock-Katalog zurücksetzen

Ereignis-ID = 4

Ebene = 4 (Informationen)

Die folgenden Winsock-LSP-Ereignisse werden bei einem Winsock-Katalog Zurücksetzungs Vorgang nachverfolgt:

-   Der Winsock-Katalog wird zurückgesetzt.

Die folgenden Parameter werden für ein Winsock-Katalog Zurücksetzungs Ereignis protokolliert:



| Parameter                                                                                        | BESCHREIBUNG                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Sieren<br/> | Der Winsock-Katalog (32-Bit oder 64-Bit), der zurückgesetzt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung](winsock-tracing-event-details.md)
</dt> </dl>

 

 
