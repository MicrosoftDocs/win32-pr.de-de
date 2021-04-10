---
title: RPC-Strukturen
description: In diesem Abschnitt werden die Strukturen erläutert, die von Microsoft RPC definiert und verwendet werden.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- Remote Prozedur Aufruf RPC, Referenz, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729401"
---
# <a name="rpc-structures"></a><span data-ttu-id="484ad-104">RPC-Strukturen</span><span class="sxs-lookup"><span data-stu-id="484ad-104">RPC Structures</span></span>

<span data-ttu-id="484ad-105">In diesem Abschnitt werden die Strukturen erläutert, die von Microsoft RPC definiert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="484ad-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="484ad-106">[**NDR \_ sContext**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="484ad-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="484ad-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="484ad-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="484ad-108">**Informationen zu NDR- \_ Benutzer \_ Mars Hall \_**</span><span class="sxs-lookup"><span data-stu-id="484ad-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="484ad-109">**NDR- \_ Benutzer \_ Mars Hall \_ Info \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="484ad-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="484ad-110">**Informationen zur asynchronen RPC- \_ \_ Benachrichtigung \_**</span><span class="sxs-lookup"><span data-stu-id="484ad-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="484ad-111">**asynchroner RPC- \_ \_ Status**</span><span class="sxs-lookup"><span data-stu-id="484ad-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="484ad-112">**RPC- \_ Bindungs \_ handle- \_ Optionen \_ v1**</span><span class="sxs-lookup"><span data-stu-id="484ad-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="484ad-113">**RPC- \_ Bindungs \_ handle- \_ Sicherheit \_ v1**</span><span class="sxs-lookup"><span data-stu-id="484ad-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="484ad-114">**RPC- \_ Bindungs \_ handle- \_ Vorlage \_ v1**</span><span class="sxs-lookup"><span data-stu-id="484ad-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="484ad-115">**RPC- \_ Bindungs \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="484ad-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="484ad-116">**RPC-C-opt-Cookie-Authentifizierungs \_ \_ \_ \_ \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="484ad-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="484ad-117">**RPC- \_ Aufruf \_ Attribute \_ v1**</span><span class="sxs-lookup"><span data-stu-id="484ad-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="484ad-118">**RPC- \_ Aufruf \_ Attribute \_ v2**</span><span class="sxs-lookup"><span data-stu-id="484ad-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="484ad-119">**RPC- \_ Aufruf- \_ lokale \_ Adresse \_ v1**</span><span class="sxs-lookup"><span data-stu-id="484ad-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="484ad-120">**RPC- \_ Client \_ Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="484ad-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="484ad-121">**RPC-Verteilungs \_ \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="484ad-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="484ad-122">**RPC- \_ EE- \_ info-Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="484ad-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="484ad-123">**RPC- \_ Endpunkt \_ Vorlage**</span><span class="sxs-lookup"><span data-stu-id="484ad-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="484ad-124">**RPC-Fehler-Aufzählungs \_ \_ \_ handle**</span><span class="sxs-lookup"><span data-stu-id="484ad-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="484ad-125">**Erweiterte RPC- \_ \_ Fehler \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="484ad-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="484ad-126">**RPC- \_ http- \_ Transport \_ Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="484ad-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="484ad-127">**RPC- \_ http- \_ Transport Anmelde Informationen \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="484ad-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="484ad-128">**RPC- \_ http- \_ Transport Anmelde Informationen \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="484ad-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="484ad-129">**RPC- \_ if- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="484ad-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="484ad-130">**RPC- \_ if- \_ ID- \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="484ad-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="484ad-131">**RPC- \_ Schnittstellen \_ Vorlage**</span><span class="sxs-lookup"><span data-stu-id="484ad-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="484ad-132">**RPC- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="484ad-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="484ad-133">**RPC- \_ protabq- \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="484ad-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="484ad-134">**RPC- \_ Sicherheits- \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="484ad-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="484ad-135">**RPC- \_ Sicherheits- \_ QoS \_ v2**</span><span class="sxs-lookup"><span data-stu-id="484ad-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="484ad-136">**RPC- \_ Sicherheits- \_ QoS \_ v3**</span><span class="sxs-lookup"><span data-stu-id="484ad-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="484ad-137">**RPC- \_ Sicherheits- \_ QoS \_ v4**</span><span class="sxs-lookup"><span data-stu-id="484ad-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="484ad-138">**RPC- \_ Sicherheits- \_ QoS \_ V5**</span><span class="sxs-lookup"><span data-stu-id="484ad-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="484ad-139">**RPC- \_ Statistik \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="484ad-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="484ad-140">**SEK \_ . WinNT-Authentifizierungs \_ \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="484ad-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="484ad-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="484ad-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="484ad-142">**UUID- \_ Vektor**</span><span class="sxs-lookup"><span data-stu-id="484ad-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 