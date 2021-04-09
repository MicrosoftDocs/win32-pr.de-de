---
title: Registrierungs Werte für das Authentifizierungsprotokoll
description: Die Setup Software für die EAP-dll erstellt möglicherweise die folgenden Registrierungs Werte unter eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104038402"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="a5c43-119">Registrierungs Werte für das Authentifizierungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="a5c43-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="a5c43-120">Die Setup Software für die EAP-dll erstellt möglicherweise die folgenden Registrierungs Werte unter **&lt; eaptypeid &gt;**.</span><span class="sxs-lookup"><span data-stu-id="a5c43-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="a5c43-121">Diese Registrierungs Werte werden in der Header Datei "raseapif. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="a5c43-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="a5c43-122">Die **RAS_EAP_VALUENAME_PATH** -und **RAS_EAP_VALUENAME_FRIENDLY_NAME** Werte sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a5c43-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="a5c43-123">Die Setup Software erstellt möglicherweise auch andere Schlüssel und Werte.</span><span class="sxs-lookup"><span data-stu-id="a5c43-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="a5c43-124">Diese können vom Authentifizierungsprotokoll selbst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5c43-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="a5c43-125">Weitere Informationen und ein Beispiel für die Registrierungs Konfiguration finden Sie unter [Beispiel für Registrierungs Werte](registry-values-example.md).</span><span class="sxs-lookup"><span data-stu-id="a5c43-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="a5c43-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="a5c43-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="a5c43-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="a5c43-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="a5c43-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="a5c43-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="a5c43-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="a5c43-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="a5c43-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="a5c43-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="a5c43-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="a5c43-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="a5c43-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="a5c43-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="a5c43-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Ich</span><span class="sxs-lookup"><span data-stu-id="a5c43-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="a5c43-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="a5c43-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="a5c43-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="a5c43-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="a5c43-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="a5c43-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="a5c43-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a5c43-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="a5c43-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a5c43-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="a5c43-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="a5c43-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="a5c43-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="a5c43-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="a5c43-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="a5c43-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="a5c43-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="a5c43-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="a5c43-143">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-143">Constant value</span></span> | <span data-ttu-id="a5c43-144">`Path`</span><span class="sxs-lookup"><span data-stu-id="a5c43-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="a5c43-145">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-145">Type</span></span>           | <span data-ttu-id="a5c43-146">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="a5c43-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="a5c43-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-147">Description</span></span>    | <span data-ttu-id="a5c43-148">Gibt den Pfad zur EAP-dll an.</span><span class="sxs-lookup"><span data-stu-id="a5c43-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="a5c43-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="a5c43-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="a5c43-150">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-150">Constant value</span></span> | <span data-ttu-id="a5c43-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a5c43-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-152">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-152">Type</span></span>           | <span data-ttu-id="a5c43-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a5c43-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="a5c43-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-154">Description</span></span>    | <span data-ttu-id="a5c43-155">Gibt einen anzeigen Amen für das Authentifizierungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="a5c43-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="a5c43-156">Dieser Name wird in der Benutzeroberfläche der EAP-Anwendung sowohl für Einwähl-als auch für drahtlose Implementierungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5c43-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="a5c43-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="a5c43-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="a5c43-158">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-158">Constant value</span></span> | <span data-ttu-id="a5c43-159">Configuipath</span><span class="sxs-lookup"><span data-stu-id="a5c43-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-160">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-160">Type</span></span>           | <span data-ttu-id="a5c43-161">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="a5c43-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="a5c43-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-162">Description</span></span>    | <span data-ttu-id="a5c43-163">Gibt den Pfad zu der dll an, die die Benutzeroberfläche für die Konfiguration auf dem Client implementiert, da diese Benutzeroberfläche ausschließlich für Client vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="a5c43-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="a5c43-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="a5c43-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="a5c43-165">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-165">Constant value</span></span> | <span data-ttu-id="a5c43-166">ConfigData</span><span class="sxs-lookup"><span data-stu-id="a5c43-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a5c43-167">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-167">Type</span></span>           | <span data-ttu-id="a5c43-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a5c43-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="a5c43-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-169">Description</span></span>    | <span data-ttu-id="a5c43-170">Gibt Standard Konfigurationsdaten für das Authentifizierungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="a5c43-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="a5c43-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="a5c43-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="a5c43-172">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-172">Constant value</span></span> | <span data-ttu-id="a5c43-173">Requirements configui</span><span class="sxs-lookup"><span data-stu-id="a5c43-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-174">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-174">Type</span></span>           | <span data-ttu-id="a5c43-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="a5c43-176">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-176">Description</span></span>    | <span data-ttu-id="a5c43-177">Gibt an, ob der Benutzer Konfigurationsdaten in der Benutzeroberfläche der EAP-Client Anwendung bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="a5c43-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="a5c43-178">Wenn dieser Wert 1 ist, kann der Benutzer die Benutzeroberfläche der EAP-Client Anwendung nicht beenden, ohne Konfigurationsdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a5c43-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="a5c43-179">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a5c43-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="a5c43-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="a5c43-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="a5c43-181">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-181">Constant value</span></span> | <span data-ttu-id="a5c43-182">Configclsid</span><span class="sxs-lookup"><span data-stu-id="a5c43-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="a5c43-183">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-183">Type</span></span>           | <span data-ttu-id="a5c43-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a5c43-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="a5c43-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-185">Description</span></span>    | <span data-ttu-id="a5c43-186">Gibt die Klassen-ID der Konfigurations Benutzeroberfläche auf dem Server an.</span><span class="sxs-lookup"><span data-stu-id="a5c43-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="a5c43-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="a5c43-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="a5c43-188">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-188">Constant value</span></span> | <span data-ttu-id="a5c43-189">Identitypath</span><span class="sxs-lookup"><span data-stu-id="a5c43-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-190">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-190">Type</span></span>           | <span data-ttu-id="a5c43-191">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="a5c43-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="a5c43-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-192">Description</span></span>    | <span data-ttu-id="a5c43-193">Gibt den Pfad zu der dll an, die Funktionen implementiert, um die Benutzeridentität auf dem Client abzurufen, da diese Benutzeroberfläche nur für den Client bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="a5c43-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="a5c43-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="a5c43-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="a5c43-195">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-195">Constant value</span></span> | <span data-ttu-id="a5c43-196">Interactiveuipath</span><span class="sxs-lookup"><span data-stu-id="a5c43-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-197">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-197">Type</span></span>           | <span data-ttu-id="a5c43-198">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="a5c43-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="a5c43-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-199">Description</span></span>    | <span data-ttu-id="a5c43-200">Gibt den Pfad zu der dll an, die die interaktive Benutzeroberfläche auf dem Client implementiert, da diese Benutzeroberfläche nur für den Client bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="a5c43-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="a5c43-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="a5c43-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="a5c43-202">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-202">Constant value</span></span> | <span data-ttu-id="a5c43-203">Invokeusernamedialog</span><span class="sxs-lookup"><span data-stu-id="a5c43-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-204">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-204">Type</span></span>           | <span data-ttu-id="a5c43-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a5c43-206">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-206">Description</span></span>    | <span data-ttu-id="a5c43-207">Gibt an, ob RAS das Standard Dialogfeld für Windows NT/Windows 2000-Benutzername (Wert 1) oder [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (Wert 0) anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="a5c43-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="a5c43-208">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="a5c43-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="a5c43-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="a5c43-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="a5c43-210">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-210">Constant value</span></span> | <span data-ttu-id="a5c43-211">Invokepassworddialog</span><span class="sxs-lookup"><span data-stu-id="a5c43-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-212">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-212">Type</span></span>           | <span data-ttu-id="a5c43-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="a5c43-214">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-214">Description</span></span>    | <span data-ttu-id="a5c43-215">Gibt an, ob RAS das Standard Dialogfeld Windows NT/Windows 2000-Kennwort anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="a5c43-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="a5c43-216">Wenn dieser Wert vorhanden ist und 0 ist, zeigt RAS das Kenn Wort Dialogfeld nicht an.</span><span class="sxs-lookup"><span data-stu-id="a5c43-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="a5c43-217">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="a5c43-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="a5c43-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="a5c43-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="a5c43-219">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-219">Constant value</span></span> | <span data-ttu-id="a5c43-220">Mppeer-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a5c43-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-221">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-221">Type</span></span>           | <span data-ttu-id="a5c43-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="a5c43-223">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-223">Description</span></span>    | <span data-ttu-id="a5c43-224">Wenn dieser Wert 1 ist, kann das Authentifizierungsprotokoll Schlüssel für den Microsoft-MPPE-Verschlüsselungs Stil (Point-to-Point Encryption, MPPE) generieren.</span><span class="sxs-lookup"><span data-stu-id="a5c43-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="a5c43-225">Mögliche Werte sind 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="a5c43-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="a5c43-226">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="a5c43-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="a5c43-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a5c43-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="a5c43-228">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-228">Constant value</span></span> | <span data-ttu-id="a5c43-229">Standalonesupportiert</span><span class="sxs-lookup"><span data-stu-id="a5c43-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-230">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-230">Type</span></span>           | <span data-ttu-id="a5c43-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="a5c43-232">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-232">Description</span></span>    | <span data-ttu-id="a5c43-233">Gibt an, ob dieses Authentifizierungsprotokoll auf einem eigenständigen Windows 2000-Server unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a5c43-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="a5c43-234">Der Wert 0 gibt an, dass EAP nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a5c43-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="a5c43-235">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="a5c43-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="a5c43-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a5c43-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="a5c43-237">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-237">Constant Value</span></span> | <span data-ttu-id="a5c43-238">Rolessupported</span><span class="sxs-lookup"><span data-stu-id="a5c43-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c43-239">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-239">Type</span></span>           | <span data-ttu-id="a5c43-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="a5c43-241">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-241">Description</span></span>    | <span data-ttu-id="a5c43-242">Gibt die verschiedenen Rollen an, die das EAP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5c43-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="a5c43-243">Dies gibt an, ob es auf einem Server oder Client verwendet werden kann, ob es für RAS-Verbindungen (VPN) oder PEAP unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a5c43-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="a5c43-244">Das Standardverhalten besteht darin, die EAP-Methode in PEAP und in EAP anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a5c43-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="a5c43-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="a5c43-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="a5c43-246">Konstanter Wert</span><span class="sxs-lookup"><span data-stu-id="a5c43-246">Constant Value</span></span> | <span data-ttu-id="a5c43-247">Perpolicyconfig</span><span class="sxs-lookup"><span data-stu-id="a5c43-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="a5c43-248">type</span><span class="sxs-lookup"><span data-stu-id="a5c43-248">Type</span></span>           | <span data-ttu-id="a5c43-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c43-249">REG_DWORD</span></span>      |
| <span data-ttu-id="a5c43-250">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5c43-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="a5c43-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="a5c43-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="a5c43-252">Dieser Registrierungs Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5c43-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="a5c43-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="a5c43-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="a5c43-254">Dieser Registrierungs Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5c43-254">This registry value is not in use.</span></span>

