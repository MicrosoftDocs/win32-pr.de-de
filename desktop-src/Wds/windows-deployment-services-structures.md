---
title: Windows Bereitstellungsdienstestrukturen
description: Die folgenden Strukturen werden mit den Windows verwendet.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760250"
---
# <a name="windows-deployment-services-structures"></a>Windows Bereitstellungsdienstestrukturen

Die folgenden Strukturen werden mit den Windows verwendet.



| Struktur                                                                         | Beschreibung                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PXE-ADRESSE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Gibt die Netzwerkadresse für ein Paket an.                                                                        |
| [**\_PXE-DHCP-NACHRICHT \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Diese Struktur wird mit der PXE Windows-Server-API der Bereitstellungsdienste verwendet.                                        |
| [**\_PXE-DHCP-OPTION \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Diese Struktur wird mit der PXE Windows-Server-API der Bereitstellungsdienste verwendet.                                        |
| [**PXE-ANBIETER \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Beschreibt einen Anbieter.                                                                                              |
| [**WDS \_ CLI \_ CRED**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Enthält Anmeldeinformationen, die zum Autorisieren einer Clientsitzung verwendet werden.                                                           |
| [**\_WDS-TRANSPORTCLIENT-ANFORDERUNG \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Wird von der [**WdsTransportClientStartSession-Funktion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) verwendet.                     |
| [**\_TRANSPORTCLIENT-SITZUNGSINFORMATIONEN \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Wird von der [*\_ PFN-Rückruffunktion WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) verwendet. |
| [**WDS \_ TRANSPORTPROVIDER \_ INIT \_ PARAMS**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Wird von der [**WdsTransportProviderInitialize-Rückruffunktion**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) verwendet.            |
| [**\_WDS-TRANSPORTPROVIDER-EINSTELLUNGEN \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Wird von der [**WdsTransportProviderInitialize-Rückruffunktion**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) verwendet.            |



 

Folgendes ist ab Windows 8 und Windows Server 2012.

| Struktur                                          | Beschreibung                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**\_PXE-DHCPV6-OPTION \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Wird mit der Windows Deployment Services-PXE-Server-API verwendet. |
| [**\_PXE-DHCPV6-NACHRICHT \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Eine DHCPV6-Nachricht.                                         |



 

 

 




