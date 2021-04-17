---
title: Neues in der Windows-Filter Plattform
description: Windows 8 und Windows Server 2012 führen neue Programmier Elemente für die Windows-Filter Plattform ein.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339877"
---
# <a name="whats-new-in-windows-filtering-platform"></a><span data-ttu-id="958dc-103">Neues in der Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="958dc-103">What's New in Windows Filtering Platform</span></span>

<span data-ttu-id="958dc-104">Windows 8 und Windows Server 2012 führen neue Programmier Elemente für die Windows-Filter Plattform ein.</span><span class="sxs-lookup"><span data-stu-id="958dc-104">Windows 8 and Windows Server 2012 introduce new Windows Filtering Platform programming elements.</span></span> <span data-ttu-id="958dc-105">Zu den neuen Funktionen gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="958dc-105">New functionality includes the following:</span></span>

-   <span data-ttu-id="958dc-106">*Layer 2-Filterung*: ermöglicht den Zugriff auf die L2-Ebene (Mac), sodass der Datenverkehr auf dieser Ebene gefiltert werden kann.</span><span class="sxs-lookup"><span data-stu-id="958dc-106">*Layer 2 filtering*: Provides access to the L2 (MAC) layer, allowing filtering of traffic at that layer.</span></span>
-   <span data-ttu-id="958dc-107">*vSwitch-Filterung*: ermöglicht das überprüfen und/oder Ändern von Paketen, die einen Vswitch durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="958dc-107">*vSwitch filtering*: Allows packets traversing a vSwitch to be inspected and/or modified.</span></span> <span data-ttu-id="958dc-108">WFP-Filter oder-Legenden können bei der eingehenden und ausgehenden Vswitch-Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="958dc-108">WFP filters or callouts can be used at the vSwitch ingress and egress.</span></span>
-   <span data-ttu-id="958dc-109">*Verwaltung von App*-Containern: ermöglicht den Zugriff auf Informationen zu app-Containern und Verbindungsproblemen bei der Netzwerk Isolation.</span><span class="sxs-lookup"><span data-stu-id="958dc-109">*App container management*: Allows access to information about app containers and network isolation connectivity issues.</span></span>
-   <span data-ttu-id="958dc-110">*IPSec-Updates*: Erweiterte IPsec-Funktionalität, einschließlich Verbindungsstatus Überwachung, Zertifikat Auswahl und Schlüsselverwaltung.</span><span class="sxs-lookup"><span data-stu-id="958dc-110">*IPsec updates*: Extended IPsec functionality including connection state monitoring, certificate selection, and key management.</span></span>

<span data-ttu-id="958dc-111">Das Windows-Treiberkit enthält auch Informationen zu [WFP-Änderungen für Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span><span class="sxs-lookup"><span data-stu-id="958dc-111">The Windows Driver Kit also includes information on [WFP Changes for Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span></span>

## <a name="windows-8-api-updates"></a><span data-ttu-id="958dc-112">Windows 8-API-Updates</span><span class="sxs-lookup"><span data-stu-id="958dc-112">Windows 8 API updates</span></span>

<span data-ttu-id="958dc-113">Für Windows 8 und Windows Server 2012 wurden viele neue APIs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="958dc-113">Many new APIs have been added for Windows 8 and Windows Server 2012.</span></span>

## <a name="new-functions"></a><span data-ttu-id="958dc-114">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="958dc-114">New functions</span></span>

-   [<span data-ttu-id="958dc-115">**F- \_ net- \_ Ereignis \_ CALLBACK1**</span><span class="sxs-lookup"><span data-stu-id="958dc-115">**FWPM\_NET\_EVENT\_CALLBACK1**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [<span data-ttu-id="958dc-116">**FwpmConnectionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="958dc-116">**FwpmConnectionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [<span data-ttu-id="958dc-117">**FwpmConnectionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="958dc-117">**FwpmConnectionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [<span data-ttu-id="958dc-118">**FwpmConnectionEnum0**</span><span class="sxs-lookup"><span data-stu-id="958dc-118">**FwpmConnectionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [<span data-ttu-id="958dc-119">**FwpmConnectionGetById0**</span><span class="sxs-lookup"><span data-stu-id="958dc-119">**FwpmConnectionGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [<span data-ttu-id="958dc-120">**FwpmConnectionGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="958dc-120">**FwpmConnectionGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [<span data-ttu-id="958dc-121">**FwpmConnectionSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="958dc-121">**FwpmConnectionSetSecurityInfo0**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [<span data-ttu-id="958dc-122">**FwpmConnectionSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="958dc-122">**FwpmConnectionSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [<span data-ttu-id="958dc-123">**FwpmConnectionSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="958dc-123">**FwpmConnectionSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [<span data-ttu-id="958dc-124">**FwpmConnectionUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="958dc-124">**FwpmConnectionUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [<span data-ttu-id="958dc-125">**FwpmIPsecTunnelAdd2**</span><span class="sxs-lookup"><span data-stu-id="958dc-125">**FwpmIPsecTunnelAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [<span data-ttu-id="958dc-126">**FwpmNetEventEnum2**</span><span class="sxs-lookup"><span data-stu-id="958dc-126">**FwpmNetEventEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [<span data-ttu-id="958dc-127">**FwpmNetEventSubscribe1**</span><span class="sxs-lookup"><span data-stu-id="958dc-127">**FwpmNetEventSubscribe1**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [<span data-ttu-id="958dc-128">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="958dc-128">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="958dc-129">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="958dc-129">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="958dc-130">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="958dc-130">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="958dc-131">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="958dc-131">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="958dc-132">**FwpmvSwitchEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="958dc-132">**FwpmvSwitchEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [<span data-ttu-id="958dc-133">**FwpmvSwitchEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="958dc-133">**FwpmvSwitchEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [<span data-ttu-id="958dc-134">**FwpmvSwitchEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="958dc-134">**FwpmvSwitchEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [<span data-ttu-id="958dc-135">**FwpmvSwitchEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="958dc-135">**FwpmvSwitchEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [<span data-ttu-id="958dc-136">**IkeextSaEnum2**</span><span class="sxs-lookup"><span data-stu-id="958dc-136">**IkeextSaEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [<span data-ttu-id="958dc-137">**IkeextSaGetById2**</span><span class="sxs-lookup"><span data-stu-id="958dc-137">**IkeextSaGetById2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [<span data-ttu-id="958dc-138">**IPSec-Schlüssel- \_ \_ Manager- \_ Schlüssel \_ Diktat \_ CHECK0**</span><span class="sxs-lookup"><span data-stu-id="958dc-138">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="958dc-139">**IPSec- \_ Schlüssel- \_ Manager \_ \_ Key0 vorschreiben**</span><span class="sxs-lookup"><span data-stu-id="958dc-139">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="958dc-140">**IPSec- \_ Schlüssel- \_ Manager \_ Benachrichtigen \_ Key0**</span><span class="sxs-lookup"><span data-stu-id="958dc-140">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="958dc-141">**IPSec- \_ sa- \_ Kontext \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="958dc-141">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="958dc-142">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="958dc-142">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="958dc-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="958dc-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="958dc-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="958dc-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="958dc-145">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="958dc-145">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="958dc-146">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="958dc-146">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [<span data-ttu-id="958dc-147">**IPsecSaContextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="958dc-147">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="958dc-148">**IPsecSaContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="958dc-148">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="958dc-149">**IPsecSaContextUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="958dc-149">**IPsecSaContextUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [<span data-ttu-id="958dc-150">**Networkisolationdiagnoseconnectfailureandgetinfo**</span><span class="sxs-lookup"><span data-stu-id="958dc-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [<span data-ttu-id="958dc-151">**Networkisolationeinumappcontainers**</span><span class="sxs-lookup"><span data-stu-id="958dc-151">**NetworkIsolationEnumAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [<span data-ttu-id="958dc-152">**Networkisolationenumerateappcontainerrules**</span><span class="sxs-lookup"><span data-stu-id="958dc-152">**NetworkIsolationEnumerateAppContainerRules**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [<span data-ttu-id="958dc-153">**Networkisolationfreappcontainers**</span><span class="sxs-lookup"><span data-stu-id="958dc-153">**NetworkIsolationFreeAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [<span data-ttu-id="958dc-154">**Networkisolationgetappcontainerconfig**</span><span class="sxs-lookup"><span data-stu-id="958dc-154">**NetworkIsolationGetAppContainerConfig**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [<span data-ttu-id="958dc-155">**Networkisolationregisterforappcontainerchanges**</span><span class="sxs-lookup"><span data-stu-id="958dc-155">**NetworkIsolationRegisterForAppContainerChanges**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [<span data-ttu-id="958dc-156">**Networkisolationabtappcontainerconfig**</span><span class="sxs-lookup"><span data-stu-id="958dc-156">**NetworkIsolationSetAppContainerConfig**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [<span data-ttu-id="958dc-157">**Networkisolationsetupappcontainerbinaries**</span><span class="sxs-lookup"><span data-stu-id="958dc-157">**NetworkIsolationSetupAppContainerBinaries**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [<span data-ttu-id="958dc-158">**PAC- \_ Änderungs \_ Rückruf- \_ FN**</span><span class="sxs-lookup"><span data-stu-id="958dc-158">**PAC\_CHANGES\_CALLBACK\_FN**</span></span>](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a><span data-ttu-id="958dc-159">Neue Strukturen</span><span class="sxs-lookup"><span data-stu-id="958dc-159">New structures</span></span>

-   [<span data-ttu-id="958dc-160">**Ikeext- \_ Authentifizierung \_ Methode2**</span><span class="sxs-lookup"><span data-stu-id="958dc-160">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="958dc-161">**Ikeext \_ CERT \_ EKUS0**</span><span class="sxs-lookup"><span data-stu-id="958dc-161">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="958dc-162">**Ikeext \_ CERT \_ NAME0**</span><span class="sxs-lookup"><span data-stu-id="958dc-162">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="958dc-163">**Ikeext- \_ Zertifikat \_ fügen**</span><span class="sxs-lookup"><span data-stu-id="958dc-163">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="958dc-164">**Ikeext- \_ Zertifikat \_ CRITERIA0**</span><span class="sxs-lookup"><span data-stu-id="958dc-164">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="958dc-165">**Ikeext \_ EM \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="958dc-165">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="958dc-166">**Ikeext \_ Kerberos \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="958dc-166">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="958dc-167">**Ikeext \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="958dc-167">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="958dc-168">**IPSec- \_ Schlüssel \_ MANAGER0**</span><span class="sxs-lookup"><span data-stu-id="958dc-168">**IPSEC\_KEY\_MANAGER0**</span></span>](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [<span data-ttu-id="958dc-169">**IPSec- \_ Schlüssel- \_ Manager \_ CALLBACKS0**</span><span class="sxs-lookup"><span data-stu-id="958dc-169">**IPSEC\_KEY\_MANAGER\_CALLBACKS0**</span></span>](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [<span data-ttu-id="958dc-170">**IPSec-Schlüssel \_ \_ Richtlinie1**</span><span class="sxs-lookup"><span data-stu-id="958dc-170">**IPSEC\_KEYING\_POLICY1**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [<span data-ttu-id="958dc-171">**IPSec- \_ sa- \_ Kontext \_ CHANGE0**</span><span class="sxs-lookup"><span data-stu-id="958dc-171">**IPSEC\_SA\_CONTEXT\_CHANGE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [<span data-ttu-id="958dc-172">**IPSec- \_ sa- \_ Kontext \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="958dc-172">**IPSEC\_SA\_CONTEXT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [<span data-ttu-id="958dc-173">**IPSec- \_ Transport \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="958dc-173">**IPSEC\_TRANSPORT\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [<span data-ttu-id="958dc-174">**IPSec- \_ Tunnel \_ ENDPOINT0**</span><span class="sxs-lookup"><span data-stu-id="958dc-174">**IPSEC\_TUNNEL\_ENDPOINT0**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [<span data-ttu-id="958dc-175">**IPSec- \_ Tunnel \_ ENDPOINTS2**</span><span class="sxs-lookup"><span data-stu-id="958dc-175">**IPSEC\_TUNNEL\_ENDPOINTS2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [<span data-ttu-id="958dc-176">**IPSec- \_ Tunnel \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="958dc-176">**IPSEC\_TUNNEL\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [<span data-ttu-id="958dc-177">**\_CONNECTION0**</span><span class="sxs-lookup"><span data-stu-id="958dc-177">**FWPM\_CONNECTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [<span data-ttu-id="958dc-178">**WPM- \_ Verbindungs Aufzählung \_ \_ TEMPLATE0**</span><span class="sxs-lookup"><span data-stu-id="958dc-178">**FWPM\_CONNECTION\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [<span data-ttu-id="958dc-179">**Verbindung mit der \_ SUBSCRIPTION0-Verbindung \_**</span><span class="sxs-lookup"><span data-stu-id="958dc-179">**FWPM\_CONNECTION\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [<span data-ttu-id="958dc-180">**F \_ \_ EVENT2**</span><span class="sxs-lookup"><span data-stu-id="958dc-180">**FWPM\_NET\_EVENT2**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [<span data-ttu-id="958dc-181">**BPM \_ net- \_ Ereignis \_ Funktion \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="958dc-181">**FWPM\_NET\_EVENT\_CAPABILITY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [<span data-ttu-id="958dc-182">**BPM \_ net- \_ Ereignis \_ Funktion \_ DROP0**</span><span class="sxs-lookup"><span data-stu-id="958dc-182">**FWPM\_NET\_EVENT\_CAPABILITY\_DROP0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [<span data-ttu-id="958dc-183">**F/a \_ - \_ Ereignis \_ Klassifizierung \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="958dc-183">**FWPM\_NET\_EVENT\_CLASSIFY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [<span data-ttu-id="958dc-184">**F/a \_ - \_ Ereignis \_ Klassifizierung \_ DROP2**</span><span class="sxs-lookup"><span data-stu-id="958dc-184">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [<span data-ttu-id="958dc-185">**Löschen eines f \_ - \_ \_ \_ \_ MAC0**</span><span class="sxs-lookup"><span data-stu-id="958dc-185">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP\_MAC0**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [<span data-ttu-id="958dc-186">**F- \_ net- \_ Ereignis \_ HEADER2**</span><span class="sxs-lookup"><span data-stu-id="958dc-186">**FWPM\_NET\_EVENT\_HEADER2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [<span data-ttu-id="958dc-187">**Swpm- \_ Anbieter \_ CONTEXT2**</span><span class="sxs-lookup"><span data-stu-id="958dc-187">**FWPM\_PROVIDER\_CONTEXT2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [<span data-ttu-id="958dc-188">**Fwpm- \_ vSwitch \_ EVENT0**</span><span class="sxs-lookup"><span data-stu-id="958dc-188">**FWPM\_VSWITCH\_EVENT0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [<span data-ttu-id="958dc-189">**Fwpm \_ vSwitch- \_ Ereignis \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="958dc-189">**FWPM\_VSWITCH\_EVENT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a><span data-ttu-id="958dc-190">Neue Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="958dc-190">New enumerated types</span></span>

-   [<span data-ttu-id="958dc-191">**FWP- \_ vSwitch- \_ \_ Netzwerktyp**</span><span class="sxs-lookup"><span data-stu-id="958dc-191">**FWP\_VSWITCH\_NETWORK\_TYPE**</span></span>](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [<span data-ttu-id="958dc-192">**atwpm- \_ APPC- \_ Netzwerk \_ \_ Funktionstyp**</span><span class="sxs-lookup"><span data-stu-id="958dc-192">**FWPM\_APPC\_NETWORK\_CAPABILITY\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [<span data-ttu-id="958dc-193">**\_ \_ Typ der Ereignis Ereignis Verbindung \_**</span><span class="sxs-lookup"><span data-stu-id="958dc-193">**FWPM\_CONNECTION\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [<span data-ttu-id="958dc-194">**fwpm \_ vSwitch \_ - \_ Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="958dc-194">**FWPM\_VSWITCH\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [<span data-ttu-id="958dc-195">**ikeext \_ CERT \_ - \_ Kriterienname- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="958dc-195">**IKEEXT\_CERT\_CRITERIA\_NAME\_TYPE**</span></span>](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [<span data-ttu-id="958dc-196">**IPSec- \_ sa- \_ Kontext \_ Ereignis \_ TYPE0**</span><span class="sxs-lookup"><span data-stu-id="958dc-196">**IPSEC\_SA\_CONTEXT\_EVENT\_TYPE0**</span></span>](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a><span data-ttu-id="958dc-197">Neue filterebenenbezeichner</span><span class="sxs-lookup"><span data-stu-id="958dc-197">New filtering layer identifiers</span></span>

[<span data-ttu-id="958dc-198">**Filtern von ebenenbezeichlern:**</span><span class="sxs-lookup"><span data-stu-id="958dc-198">**Filtering Layer Identifiers:**</span></span>](management-filtering-layer-identifiers-.md)

-   <span data-ttu-id="958dc-199">fwpm- \_ Schicht \_ eingehender Mac- \_ \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="958dc-199">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="958dc-200">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="958dc-200">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="958dc-201">fwpm- \_ Schicht, \_ eingehender Mac- \_ \_ Frame \_</span><span class="sxs-lookup"><span data-stu-id="958dc-201">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="958dc-202">\_ \_ ausgehender \_ Mac- \_ Frame \_ der fwpm-Ebene</span><span class="sxs-lookup"><span data-stu-id="958dc-202">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="958dc-203">fwpm- \_ Schicht \_ Ingress \_ vSwitch \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="958dc-203">FWPM\_LAYER\_INGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="958dc-204">fwpm- \_ Schicht, \_ ausgehender \_ vSwitch \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="958dc-204">FWPM\_LAYER\_EGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="958dc-205">Fwpm- \_ Schicht \_ Eingangs \_ -vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht Eingangs- \_ \_ vSwitch- \_ Transport \_ V6</span><span class="sxs-lookup"><span data-stu-id="958dc-205">FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>
-   <span data-ttu-id="958dc-206">Fwpm- \_ Schicht \_ ausgehender \_ vSwitch \_ \_ -Transport V4/fwpm- \_ Schicht \_ ausgehender \_ vSwitch- \_ Transport \_ V6</span><span class="sxs-lookup"><span data-stu-id="958dc-206">FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>

## <a name="new-filtering-condition-identifiers"></a><span data-ttu-id="958dc-207">Neue Filter Bedingungs Bezeichner</span><span class="sxs-lookup"><span data-stu-id="958dc-207">New filtering condition identifiers</span></span>

[<span data-ttu-id="958dc-208">**Filtern von Bedingungs bezeichlern:**</span><span class="sxs-lookup"><span data-stu-id="958dc-208">**Filtering Condition Identifiers:**</span></span>](filtering-condition-identifiers-.md)

-   <span data-ttu-id="958dc-209">Mac-Adresse der WPM-Bedingungs \_ \_ Schnittstelle \_ \_</span><span class="sxs-lookup"><span data-stu-id="958dc-209">FWPM\_CONDITION\_INTERFACE\_MAC\_ADDRESS</span></span>
-   <span data-ttu-id="958dc-210">\_ \_ lokale MAC-Adresse für \_ Mac \_</span><span class="sxs-lookup"><span data-stu-id="958dc-210">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS</span></span>
-   <span data-ttu-id="958dc-211">\_ \_ Mac- \_ Remote \_ Adresse für den WPM-Zustand</span><span class="sxs-lookup"><span data-stu-id="958dc-211">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS</span></span>
-   <span data-ttu-id="958dc-212">\_Typ der Bedingung \_ \_</span><span class="sxs-lookup"><span data-stu-id="958dc-212">FWPM\_CONDITION\_ETHER\_TYPE</span></span>
-   <span data-ttu-id="958dc-213">\_ \_ VLAN-ID für fwpm-Bedingung \_</span><span class="sxs-lookup"><span data-stu-id="958dc-213">FWPM\_CONDITION\_VLAN\_ID</span></span>
-   <span data-ttu-id="958dc-214">\_ \_ NDIS-Port der bwpm-Bedingung \_</span><span class="sxs-lookup"><span data-stu-id="958dc-214">FWPM\_CONDITION\_NDIS\_PORT</span></span>
-   <span data-ttu-id="958dc-215">\_ \_ Dateityp für den NDIS- \_ \_ Medientyp</span><span class="sxs-lookup"><span data-stu-id="958dc-215">FWPM\_CONDITION\_NDIS\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="958dc-216">\_ \_ Typ der physischen NDIS- \_ \_ \_ Medientyp</span><span class="sxs-lookup"><span data-stu-id="958dc-216">FWPM\_CONDITION\_NDIS\_PHYSICAL\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="958dc-217">WPM- \_ Bedingung \_ L2- \_ Flags</span><span class="sxs-lookup"><span data-stu-id="958dc-217">FWPM\_CONDITION\_L2\_FLAGS</span></span>
-   <span data-ttu-id="958dc-218">\_ \_ lokale MAC-Adresse für \_ den Mac- \_ \_ Typ</span><span class="sxs-lookup"><span data-stu-id="958dc-218">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="958dc-219">\_ \_ Mac- \_ Remote \_ \_ Adresstyp für die Schutz Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-219">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="958dc-220">ID des WPM-Bedingungs- \_ \_ \_ ID-Pakets \_</span><span class="sxs-lookup"><span data-stu-id="958dc-220">FWPM\_CONDITION\_ALE\_PACKAGE\_ID</span></span>
-   <span data-ttu-id="958dc-221">\_ \_ Mac- \_ Quell \_ Adresse für die lwpm-Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-221">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS</span></span>
-   <span data-ttu-id="958dc-222">\_ \_ Mac- \_ Ziel \_ Adresse der bwpm-Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-222">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS</span></span>
-   <span data-ttu-id="958dc-223">\_Typ der Mac- \_ \_ Quell \_ Adresse \_ für die Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-223">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="958dc-224">\_Typ der Mac- \_ \_ Ziel \_ Adresse \_ der bwpm-Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-224">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="958dc-225">\_ \_ IP- \_ Quellport für die IP-Adresse der Bedingung \_</span><span class="sxs-lookup"><span data-stu-id="958dc-225">FWPM\_CONDITION\_IP\_SOURCE\_PORT</span></span>
-   <span data-ttu-id="958dc-226">\_ \_ IP- \_ \_ Zielport der BPM-Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-226">FWPM\_CONDITION\_IP\_DESTINATION\_PORT</span></span>
-   <span data-ttu-id="958dc-227">fwpm-Bedingungs- \_ \_ vSwitch- \_ ID</span><span class="sxs-lookup"><span data-stu-id="958dc-227">FWPM\_CONDITION\_VSWITCH\_ID</span></span>
-   <span data-ttu-id="958dc-228">fwpm-Bedingungs- \_ \_ vSwitch- \_ \_ Netzwerktyp</span><span class="sxs-lookup"><span data-stu-id="958dc-228">FWPM\_CONDITION\_VSWITCH\_NETWORK\_TYPE</span></span>
-   <span data-ttu-id="958dc-229">fwpm-Bedingungs- \_ \_ vSwitch \_ Quell \_ Schnittstellen- \_ ID</span><span class="sxs-lookup"><span data-stu-id="958dc-229">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="958dc-230">fwpm-Bedingungs- \_ \_ vSwitch- \_ Ziel \_ Schnittstellen- \_ ID</span><span class="sxs-lookup"><span data-stu-id="958dc-230">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="958dc-231">fwpm-Bedingungs- \_ \_ vSwitch \_ Quell- \_ VM- \_ ID</span><span class="sxs-lookup"><span data-stu-id="958dc-231">FWPM\_CONDITION\_VSWITCH\_SOURCE\_VM\_ID</span></span>
-   <span data-ttu-id="958dc-232">fwpm-Bedingungs- \_ \_ vSwitch- \_ Ziel-VM- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="958dc-232">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_VM\_ID</span></span>
-   <span data-ttu-id="958dc-233">\_ \_ Typ der Vswitch- \_ Quell \_ Schnittstelle \_ für fwpm-Bedingung</span><span class="sxs-lookup"><span data-stu-id="958dc-233">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_TYPE</span></span>
-   <span data-ttu-id="958dc-234">\_ \_ \_ Netzwerk- \_ \_ ID des Vswitch-Mandanten für fwpm</span><span class="sxs-lookup"><span data-stu-id="958dc-234">FWPM\_CONDITION\_VSWITCH\_TENANT\_NETWORK\_ID</span></span>

## <a name="new-filtering-condition-flags"></a><span data-ttu-id="958dc-235">Neue filterbedingungs-Flags</span><span class="sxs-lookup"><span data-stu-id="958dc-235">New filtering condition flags</span></span>

[<span data-ttu-id="958dc-236">**Filter Bedingungs Flags:**</span><span class="sxs-lookup"><span data-stu-id="958dc-236">**Filtering Condition Flags:**</span></span>](filtering-condition-flags-.md)

-   <span data-ttu-id="958dc-237">das Flag der SWP- \_ Bedingung \_ ist eine \_ \_ Proxy \_ Verbindung.</span><span class="sxs-lookup"><span data-stu-id="958dc-237">FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION</span></span>
-   <span data-ttu-id="958dc-238">Das BWP-Bedingungs Kennzeichen \_ \_ ist " \_ \_ appcontainer \_ Loopback".</span><span class="sxs-lookup"><span data-stu-id="958dc-238">FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="958dc-239">das Flag der BWP- \_ Bedingung \_ \_ ist \_ kein \_ appcontainer- \_ Loopback.</span><span class="sxs-lookup"><span data-stu-id="958dc-239">FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="958dc-240">das Flag der SWP- \_ Bedingung \_ ist die \_ \_ \_ Autorisierung der Richtlinie \_</span><span class="sxs-lookup"><span data-stu-id="958dc-240">FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE</span></span>
-   <span data-ttu-id="958dc-241">Die f- \_ Bedingung \_ L2 \_ ist \_ natives \_ Ethernet.</span><span class="sxs-lookup"><span data-stu-id="958dc-241">FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET</span></span>
-   <span data-ttu-id="958dc-242">F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi</span><span class="sxs-lookup"><span data-stu-id="958dc-242">FWP\_CONDITION\_L2\_IS\_WIFI</span></span>
-   <span data-ttu-id="958dc-243">F WP- \_ Bedingung \_ L2 \_ ist \_ mobiles \_ Breitband</span><span class="sxs-lookup"><span data-stu-id="958dc-243">FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND</span></span>
-   <span data-ttu-id="958dc-244">F WP- \_ Bedingung \_ L2 \_ ist \_ WiFi Direct- \_ \_ Daten</span><span class="sxs-lookup"><span data-stu-id="958dc-244">FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA</span></span>
-   <span data-ttu-id="958dc-245">F- \_ Bedingung \_ L2 \_ ist \_ VM2VM</span><span class="sxs-lookup"><span data-stu-id="958dc-245">FWP\_CONDITION\_L2\_IS\_VM2VM</span></span>
-   <span data-ttu-id="958dc-246">Die f- \_ Bedingung \_ L2 \_ ist \_ falsch \_ formatiertes Paket.</span><span class="sxs-lookup"><span data-stu-id="958dc-246">FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET</span></span>
-   <span data-ttu-id="958dc-247">\_ \_ \_ \_ SWP-Bedingung L2 ist IP- \_ \_ fragmentgruppe</span><span class="sxs-lookup"><span data-stu-id="958dc-247">FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP</span></span>
-   <span data-ttu-id="958dc-248">SWP- \_ Bedingung \_ L2, \_ Wenn \_ Connector \_ vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="958dc-248">FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT</span></span>

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a><span data-ttu-id="958dc-249">Windows 7-Updates für die Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="958dc-249">Windows 7 updates to the Windows Filtering Platform</span></span>

<span data-ttu-id="958dc-250">Im Dokument [Neues in der Windows-Filter Plattform]() werden viele der für Windows 7 vorgenommenen Updates ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="958dc-250">The document [What's New in Windows Filtering Platform]() details many of the updates made for Windows 7.</span></span> <span data-ttu-id="958dc-251">Informationen finden Sie auch im Windows-Treiberkit unter [WFP-Änderungen für Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span><span class="sxs-lookup"><span data-stu-id="958dc-251">Information is also available in the Windows Driver Kit on [WFP Changes for Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span></span>

 

 