---
description: Details zur Ablaufverfolgung für Winsock-Katalogänderung
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Details zur Ablaufverfolgung für Winsock-Katalogänderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d949caf94d3b7bbbef32945c97cb3f1db258f798b84280570712ef5299cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051338"
---
# <a name="winsock-catalog-change-tracing-details"></a>Details zur Ablaufverfolgung für Winsock-Katalogänderung

> [!Note]  
> Mehrschichtige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 Windows Server 2012 [Filterplattform Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Die Ereignisablaufverfolgung für Winsock-Katalogänderung für mehrschichtige Dienstanbieter (LSPs) bezieht sich auf LSP-Installation, LSP-Entfernung, LSP-Deaktivierung und Winsock-Katalogzurücksetzungsvorgänge. Alle folgenden Ereignisse werden in den *Kanal Microsoft-Windows-Winsock-WS2HELP/Operational* geschrieben, der sich von der anderen Winsock-Netzwerkereignisablaufverfolgung ab Windows Vista ab unterscheiden.

Im Folgenden werden die einzelnen Winsock-LSP-Ereignisse beschrieben, die nachverfolgt werden können, und es wird beschrieben, welche Parameter und Informationen protokolliert werden.

## <a name="lsp-install"></a>LSP-Installation

Ereignis-ID = 1

Ebene = 4 (Informationen)

Die folgenden Winsock LSP-Ereignisse werden für einen LSP-Installationsvorgang nachverfolgt:

-   Ein Protokolleintrag wird im Winsock-Katalog installiert.

Die folgenden Parameter werden für ein LSP-Installationsereignis protokolliert:



| Parameter                                                                                                | Beschreibung                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name<br/>     | Der Name des LSP, der vom **szProtocol-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den installierten LSP erhalten wurde.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Katalog<br/>         | Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP installiert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer<br/> | Der Moduldateiname der Anwendung, die den LSP-Installationsaufruf vor sich hat.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | Der GUID-Wert des Winsock-Transportanbieters, unter dem der LSP installiert wird.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie<br/>     | Das **dwCatalogEntryId-Mitglied** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den installierten LSP.<br/>                                |



 

## <a name="lsp-uninstall"></a>LSP-Deinstallation

Ereignis-ID = 2

Ebene = 4 (Informationen)

Die folgenden Winsock LSP-Ereignisse werden für einen LSP-Deinstallationsvorgang nachverfolgt:

-   Ein Protokolleintrag wird aus dem Winsock-Katalog entfernt.

Die folgenden Parameter werden für ein LSP-Deinstallationsereignis protokolliert:



| Parameter                                                                                                | Beschreibung                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name<br/>     | Der Name des LSP, der vom **szProtocol-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den zu entfernenden LSP erhalten wurde.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Katalog<br/>         | Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP entfernt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer<br/> | Der Moduldateiname der Anwendung, die den LSP-Entfernungsaufruf abhebt.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | Der GUID-Wert des Winsock-Transportanbieters, aus dem der LSP entfernt wird.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie<br/>     | Das **dwCatalogEntryId-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den zu entfernenden LSP.<br/>                                |



 

## <a name="lsp-disable"></a>LSP Deaktivieren

Ereignis-ID = 3

Ebene = 4 (Informationen)

Die folgenden Winsock LSP-Ereignisse werden für einen LSP-Deaktivierungsvorgang nachverfolgt:

-   Ein Protokolleintrag ist im Winsock-Katalog deaktiviert.

Die folgenden Parameter werden für ein LSP-Deaktivierungsereignis protokolliert:



| Parameter                                                                                                | Beschreibung                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP-Name<br/>     | Der Name des LSP, der vom **szProtocol-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den deaktivierten LSP erhalten wurde.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Katalog<br/>         | Der Winsock-Katalog (32-Bit oder 64-Bit), in dem der LSP deaktiviert wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer<br/> | Der Moduldateiname der Anwendung, die den LSP-Deaktivierungsaufruf vor sich hat.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | Der GUID-Wert des Winsock-Transportanbieters, bei dem der LSP deaktiviert wird.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Kategorie<br/>     | Das **dwCatalogEntryId-Member** der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) für den deaktivierten LSP.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Winsock-Katalogzurücksetzung

Ereignis-ID = 4

Ebene = 4 (Informationen)

Die folgenden Winsock LSP-Ereignisse werden für einen Winsock-Katalogzurücksetzungsvorgang nachverfolgt:

-   Der Winsock-Katalog wird zurückgesetzt.

Die folgenden Parameter werden für ein Winsock-Katalogzurücksetzungsereignis protokolliert:



| Parameter                                                                                        | Beschreibung                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Katalog<br/> | Der Winsock-Katalog (32-Bit oder 64-Bit), der zurückgesetzt wird. Dies ist ein ganzzahliger Wert, der entweder 32 oder 64 ist.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Winsock Network-Ereignisablaufverfolgung](winsock-tracing-event-details.md)
</dt> </dl>

 

 
