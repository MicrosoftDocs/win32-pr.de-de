---
title: Strukturen der Windows-Bereitstellungs Dienste
description: Die folgenden Strukturen werden mit den Windows-Bereitstellungs Diensten verwendet.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037460"
---
# <a name="windows-deployment-services-structures"></a>Strukturen der Windows-Bereitstellungs Dienste

Die folgenden Strukturen werden mit den Windows-Bereitstellungs Diensten verwendet.



| Struktur                                                                         | BESCHREIBUNG                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PXE- \_ Adresse**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Gibt die Netzwerkadresse für ein Paket an.                                                                        |
| [**PXE- \_ DHCP- \_ Nachricht**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Diese Struktur wird mit der PXE-Server-API der Windows-Bereitstellungs Dienste verwendet.                                        |
| [**PXE ( \_ DHCP- \_ Option)**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Diese Struktur wird mit der PXE-Server-API der Windows-Bereitstellungs Dienste verwendet.                                        |
| [**PXE- \_ Anbieter**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Beschreibt einen Anbieter.                                                                                              |
| [**WDS- \_ CLI-Befehlszeilenschnittstelle \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Enthält Anmelde Informationen, die zum Autorisieren einer Client Sitzung verwendet werden.                                                           |
| [**WDS- \_ Transportclient- \_ Anforderung**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Wird von der [**wdstransportclientstarzession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) -Funktion verwendet.                     |
| [**Transportclient- \_ Sitzungs \_ Informationen**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Wird von der [*PFN \_ wdstransportclientsessionstartex*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) -Rückruffunktion verwendet. |
| [**WDS- \_ Transportprovider- \_ Init-Parameter \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Wird von der [**wdstransportproviderinitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) -Rückruffunktion verwendet.            |
| [**WDS- \_ Transportprovider- \_ Einstellungen**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Wird von der [**wdstransportproviderinitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) -Rückruffunktion verwendet.            |



 

Der folgende Abschnitt ist ab Windows 8 und Windows Server 2012 verfügbar.

| Struktur                                          | BESCHREIBUNG                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE- \_ DHCPv6 ( \_ Option)**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Wird mit dem PXE-Server der Windows-Bereitstellungs Dienste verwendet. |
| [**PXE- \_ DHCPv6- \_ Nachricht**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Eine DHCPv6-Meldung.                                         |



 

 

 




