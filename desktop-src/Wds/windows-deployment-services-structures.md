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
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="862ba-103">Strukturen der Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="862ba-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="862ba-104">Die folgenden Strukturen werden mit den Windows-Bereitstellungs Diensten verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="862ba-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="862ba-105">Structure</span></span>                                                                         | <span data-ttu-id="862ba-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="862ba-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="862ba-107">**PXE- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="862ba-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="862ba-108">Gibt die Netzwerkadresse für ein Paket an.</span><span class="sxs-lookup"><span data-stu-id="862ba-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="862ba-109">**PXE- \_ DHCP- \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="862ba-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="862ba-110">Diese Struktur wird mit der PXE-Server-API der Windows-Bereitstellungs Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="862ba-111">**PXE ( \_ DHCP- \_ Option)**</span><span class="sxs-lookup"><span data-stu-id="862ba-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="862ba-112">Diese Struktur wird mit der PXE-Server-API der Windows-Bereitstellungs Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="862ba-113">**PXE- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="862ba-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="862ba-114">Beschreibt einen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="862ba-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="862ba-115">**WDS- \_ CLI-Befehlszeilenschnittstelle \_**</span><span class="sxs-lookup"><span data-stu-id="862ba-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="862ba-116">Enthält Anmelde Informationen, die zum Autorisieren einer Client Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="862ba-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="862ba-117">**WDS- \_ Transportclient- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="862ba-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="862ba-118">Wird von der [**wdstransportclientstarzession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="862ba-119">**Transportclient- \_ Sitzungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="862ba-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="862ba-120">Wird von der [*PFN \_ wdstransportclientsessionstartex*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) -Rückruffunktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="862ba-121">**WDS- \_ Transportprovider- \_ Init-Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="862ba-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="862ba-122">Wird von der [**wdstransportproviderinitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) -Rückruffunktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="862ba-123">**WDS- \_ Transportprovider- \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="862ba-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="862ba-124">Wird von der [**wdstransportproviderinitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) -Rückruffunktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="862ba-125">Der folgende Abschnitt ist ab Windows 8 und Windows Server 2012 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="862ba-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="862ba-126">Struktur</span><span class="sxs-lookup"><span data-stu-id="862ba-126">Structure</span></span>                                          | <span data-ttu-id="862ba-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="862ba-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="862ba-128">**PXE- \_ DHCPv6 ( \_ Option)**</span><span class="sxs-lookup"><span data-stu-id="862ba-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="862ba-129">Wird mit dem PXE-Server der Windows-Bereitstellungs Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="862ba-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="862ba-130">**PXE- \_ DHCPv6- \_ Nachricht**</span><span class="sxs-lookup"><span data-stu-id="862ba-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="862ba-131">Eine DHCPv6-Meldung.</span><span class="sxs-lookup"><span data-stu-id="862ba-131">A DHCPV6 message.</span></span>                                         |



 

 

 




