---
title: ms-DS-repl-Authentication-Mode-Attribut
description: Das ms-DS-repl-Authentication-Mode-Attribut wird verwendet, um anzugeben, welche Authentifizierungsmethode zum Authentifizieren von Replikations Partnern verwendet wird.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- AD-Schema für das Attribut "ms-DS-repl-Authentication-Mode"
- AD-Schema für das msDS-ReplAuthenticationMode-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480359"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="58576-105">ms-DS-repl-Authentication-Mode-Attribut</span><span class="sxs-lookup"><span data-stu-id="58576-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="58576-106">Das **ms-DS-repl-Authentication-Mode** -Attribut wird verwendet, um anzugeben, welche Authentifizierungsmethode zum Authentifizieren von Replikations Partnern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58576-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="58576-107">Dieses Attribut gilt für die Konfigurations Partition einer ADAM-Instanz.</span><span class="sxs-lookup"><span data-stu-id="58576-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="58576-108">Die folgenden Werte sind die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="58576-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="58576-109">Wert</span><span class="sxs-lookup"><span data-stu-id="58576-109">Value</span></span>        | <span data-ttu-id="58576-110">Authentifizierungsmethode</span><span class="sxs-lookup"><span data-stu-id="58576-110">Authentication method</span></span>                          | <span data-ttu-id="58576-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58576-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58576-112">0</span><span class="sxs-lookup"><span data-stu-id="58576-112">0</span></span><br/> | <span data-ttu-id="58576-113">Aushandlungsdurchsatz</span><span class="sxs-lookup"><span data-stu-id="58576-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="58576-114">Alle ADAM-Instanzen im Konfigurationssatz verwenden denselben Kontonamen und dasselbe Kennwort wie das Adam-Dienst Konto.</span><span class="sxs-lookup"><span data-stu-id="58576-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="58576-115">1</span><span class="sxs-lookup"><span data-stu-id="58576-115">1</span></span><br/> | <span data-ttu-id="58576-116">Ausgehandelt</span><span class="sxs-lookup"><span data-stu-id="58576-116">Negotiated</span></span><br/>                          | <span data-ttu-id="58576-117">Zuerst wird versucht, die Kerberos-Authentifizierung (mit Dienstprinzipalnamen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="58576-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="58576-118">Falls diese nicht erfolgreich ist, wird versucht, eine NTLM-Authentifizierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="58576-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="58576-119">Wenn NTLM ausfällt, werden die ADAM-Instanzen nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="58576-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="58576-120">2</span><span class="sxs-lookup"><span data-stu-id="58576-120">2</span></span><br/> | <span data-ttu-id="58576-121">Gegenseitige Authentifizierung mithilfe von Kerberos</span><span class="sxs-lookup"><span data-stu-id="58576-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="58576-122">Kerberos-Authentifizierung mithilfe von Dienstprinzipalnamen (SPN) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58576-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="58576-123">Wenn die Kerberos-Authentifizierung fehlschlägt, werden die ADAM-Instanzen nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="58576-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="58576-124">In der folgenden Tabelle sind die programmgesteuerten Bezeichner für die Werte dieses Attributs enthalten.</span><span class="sxs-lookup"><span data-stu-id="58576-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="58576-125">Wert</span><span class="sxs-lookup"><span data-stu-id="58576-125">Value</span></span>        | <span data-ttu-id="58576-126">Bezeichner (von NTDSAPI. h)</span><span class="sxs-lookup"><span data-stu-id="58576-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="58576-127">0</span><span class="sxs-lookup"><span data-stu-id="58576-127">0</span></span><br/> | <span data-ttu-id="58576-128">**Adam \_ repl \_ Authentication \_ Mode \_ aushandeln \_ Pass- \_ through**</span><span class="sxs-lookup"><span data-stu-id="58576-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="58576-129">1</span><span class="sxs-lookup"><span data-stu-id="58576-129">1</span></span><br/> | <span data-ttu-id="58576-130">**Adam \_ repl- \_ Authentifizierungs \_ Modus- \_ Aushandlung**</span><span class="sxs-lookup"><span data-stu-id="58576-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="58576-131">2</span><span class="sxs-lookup"><span data-stu-id="58576-131">2</span></span><br/> | <span data-ttu-id="58576-132">**die \_ \_ gegenseitige Authentifizierung des Adam repl-Authentifizierungs \_ Modus ist \_ \_ \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="58576-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="58576-133">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58576-133">Entry</span></span> | <span data-ttu-id="58576-134">Wert</span><span class="sxs-lookup"><span data-stu-id="58576-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="58576-135">CN</span><span class="sxs-lookup"><span data-stu-id="58576-135">CN</span></span>                | <span data-ttu-id="58576-136">ms-DS-repl-Authentifizierungsmodus</span><span class="sxs-lookup"><span data-stu-id="58576-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="58576-137">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="58576-137">Ldap-Display-Name</span></span> | <span data-ttu-id="58576-138">msDS-ReplAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="58576-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="58576-139">Size</span><span class="sxs-lookup"><span data-stu-id="58576-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="58576-140">Berechtigung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="58576-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="58576-141">Aktualisierungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="58576-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="58576-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="58576-142">Attribute-Id</span></span>      | <span data-ttu-id="58576-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="58576-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="58576-144">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="58576-144">System-Id-Guid</span></span>    | <span data-ttu-id="58576-145">6e124d4f -1a3b-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="58576-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="58576-146">Syntax</span><span class="sxs-lookup"><span data-stu-id="58576-146">Syntax</span></span>            | [<span data-ttu-id="58576-147">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="58576-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="58576-148">Implementierungen</span><span class="sxs-lookup"><span data-stu-id="58576-148">Implementations</span></span>

-   [<span data-ttu-id="58576-149">**Adam**</span><span class="sxs-lookup"><span data-stu-id="58576-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="58576-150">Adam</span><span class="sxs-lookup"><span data-stu-id="58576-150">ADAM</span></span>



| <span data-ttu-id="58576-151">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58576-151">Entry</span></span> | <span data-ttu-id="58576-152">Wert</span><span class="sxs-lookup"><span data-stu-id="58576-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="58576-153">Link-ID</span><span class="sxs-lookup"><span data-stu-id="58576-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="58576-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="58576-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="58576-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="58576-155">System-Only</span></span>            | <span data-ttu-id="58576-156">False</span><span class="sxs-lookup"><span data-stu-id="58576-156">False</span></span>                                               |
| <span data-ttu-id="58576-157">Ist-einwertig</span><span class="sxs-lookup"><span data-stu-id="58576-157">Is-Single-Valued</span></span>       | <span data-ttu-id="58576-158">Richtig</span><span class="sxs-lookup"><span data-stu-id="58576-158">True</span></span>                                                |
| <span data-ttu-id="58576-159">Ist indiziert</span><span class="sxs-lookup"><span data-stu-id="58576-159">Is Indexed</span></span>             | <span data-ttu-id="58576-160">False</span><span class="sxs-lookup"><span data-stu-id="58576-160">False</span></span>                                               |
| <span data-ttu-id="58576-161">Im globalen Katalog</span><span class="sxs-lookup"><span data-stu-id="58576-161">In Global Catalog</span></span>      | <span data-ttu-id="58576-162">False</span><span class="sxs-lookup"><span data-stu-id="58576-162">False</span></span>                                               |
| <span data-ttu-id="58576-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="58576-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="58576-164">o:Bag: schlecht: S:</span><span class="sxs-lookup"><span data-stu-id="58576-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="58576-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="58576-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="58576-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="58576-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="58576-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="58576-167">Search-Flags</span></span>           | <span data-ttu-id="58576-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="58576-168">0x00000000</span></span>                                          |
| <span data-ttu-id="58576-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="58576-169">System-Flags</span></span>           | <span data-ttu-id="58576-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="58576-170">0x00000010</span></span>                                          |
| <span data-ttu-id="58576-171">In verwendete Klassen</span><span class="sxs-lookup"><span data-stu-id="58576-171">Classes used in</span></span>        | [<span data-ttu-id="58576-172">**Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="58576-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 





