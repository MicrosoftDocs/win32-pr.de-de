---
title: Registrierungswerte des Authentifizierungsprotokolls
description: Die Setupsoftware für die EAP-DLL erstellt möglicherweise die folgenden Registrierungswerte unter eaptypeid.
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
ms.openlocfilehash: a0822e7abb62aad136a3abbe36ee92f5b6f1ec9fbeabd6426c039f05c1f752d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739560"
---
# <a name="authentication-protocol-registry-values"></a>Registrierungswerte des Authentifizierungsprotokolls

Die Setupsoftware für die EAP-DLL kann die folgenden Registrierungswerte unter **&lt; eaptypeid &gt;** erstellen. Diese Registrierungswerte werden in der Headerdatei Raseapif.h definiert. Die **werte RAS_EAP_VALUENAME_PATH** und **RAS_EAP_VALUENAME_FRIENDLY_NAME** sind erforderlich. Die Setupsoftware kann auch andere Schlüssel und Werte erstellen. Diese können vom Authentifizierungsprotokoll selbst verwendet werden. Weitere Informationen und ein Beispiel für die Registrierungskonfiguration finden Sie unter Beispiel für [Registrierungswerte.](registry-values-example.md)

[RAS_EAP_VALUENAME_PATH](#ras_eap_valuename_path)

[RAS_EAP_VALUENAME_FRIENDLY_NAME](#ras_eap_valuename_friendly_name)

[RAS_EAP_VALUENAME_CONFIGUI](#ras_eap_valuename_configui)

[RAS_EAP_VALUENAME_DEFAULT_DATA](#ras_eap_valuename_default_data)

[RAS_EAP_VALUENAME_REQUIRE_CONFIGUI](#ras_eap_valuename_require_configui)

[RAS_EAP_VALUENAME_CONFIG_CLSID](#ras_eap_valuename_config_clsid)

[RAS_EAP_VALUENAME_IDENTITY](#ras_eap_valuename_identity)

[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Ich

[RAS_EAP_VALUENAME_INVOKE_NAMEDLG](#ras_eap_valuename_invoke_namedlg)

[RAS_EAP_VALUENAME_INVOKE_PWDDLG](#ras_eap_valuename_invoke_pwddlg)

[RAS_EAP_VALUENAME_ENCRYPTION](#ras_eap_valuename_encryption)

[RAS_EAP_VALUENAME_STANDALONE_SUPPORTED](#ras_eap_valuename_standalone_supported)

[RAS_EAP_VALUENAME_ROLES_SUPPORTED](#ras_eap_valuename_roles_supported)

[RAS_EAP_VALUENAME_PER_POLICY_CONFIG](#ras_eap_valuename_per_policy_config)

[RAS_EAP_VALUENAME_ISTUNNEL_METHOD](#ras_eap_valuename_istunnel_method)

[RAS_EAP_VALUENAME_FILTER_INNERMETHODS](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a>RAS_EAP_VALUENAME_PATH

| Konstanter Wert | `Path`                               |
|----------------|------------------------------------|
| type           | Reg_expand_sz                    |
| Beschreibung    | Gibt den Pfad zur EAP-DLL an. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Konstanter Wert | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_SZ                                                                                                                                                           |
| Beschreibung    | Gibt einen Anzeigenamen für das Authentifizierungsprotokoll an. Dieser Name wird auf der Benutzeroberfläche der EAP-Anwendung für DFÜ- und Drahtlosimplementierungen angezeigt. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Konstanter Wert | ConfigUIPath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| type           | Reg_expand_sz                                                                                                                   |
| Beschreibung    | Gibt den Pfad zur DLL an, die die Benutzeroberfläche für die Konfiguration auf dem Client implementiert, da diese Benutzeroberfläche nur für den Client bestimmt ist. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Konstanter Wert | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| type           | REG_BINARY                                                           |
| Beschreibung    | Gibt Standardkonfigurationsdaten für das Authentifizierungsprotokoll an. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Konstanter Wert | RequireConfigUI                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                                                                               |
| Beschreibung    | Gibt an, ob der Benutzer Konfigurationsdaten auf der Benutzeroberfläche der EAP-Clientanwendung bereitstellen muss. Wenn dieser Wert 1 ist, darf der Benutzer die Benutzeroberfläche der EAP-Clientanwendung nicht beenden, ohne Konfigurationsdaten bereitzustellen. Der Standardwert ist 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Konstanter Wert | ConfigCLSID                                                   |
|----------------|---------------------------------------------------------------|
| type           | REG_SZ                                                       |
| Beschreibung    | Gibt die Klassen-ID der Konfigurationsbenutzeroberfläche auf dem Server an. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Konstanter Wert | IdentityPath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| type           | Reg_expand_sz                                                                                                                        |
| Beschreibung    | Gibt den Pfad zur DLL an, die Funktionen implementiert, um die Benutzeridentität auf dem Client abzurufen, da diese Benutzeroberfläche nur für den Client bestimmt ist. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Konstanter Wert | InteractiveUIPath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| type           | Reg_expand_sz                                                                                                                 |
| Beschreibung    | Gibt den Pfad zur DLL an, die die interaktive Benutzeroberfläche auf dem Client implementiert, da diese Benutzeroberfläche nur für Clients bestimmt ist. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Konstanter Wert | InvokeUsernameDialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                             |
| Beschreibung    | Gibt an, ob RAS das Standarddialogfeld Windows NT/Windows 2000-Benutzername (Wert 1) anzeigen oder [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) aufrufen soll (Wert 0). Der Standardwert ist 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Konstanter Wert | InvokePasswordDialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                  |
| Beschreibung    | Gibt an, ob RAS das Standarddialogfeld Windows NT/Windows 2000-Kennworts anzeigen soll. Wenn dieser Wert vorhanden ist und 0 ist, zeigt RAS das Kennwortdialogfeld nicht an. Der Standardwert ist 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Konstanter Wert | MPPEEncryptionSupported                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                    |
| Beschreibung    | Wenn dieser Wert 1 ist, kann das Authentifizierungsprotokoll Schlüssel für den MPPE-Verschlüsselungsstil (Microsoft Point-to-Point Encryption) generieren. Mögliche Werte sind 0 oder 1. Der Standardwert ist 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Konstanter Wert | StandaloneSupported                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                     |
| Beschreibung    | Gibt an, ob dieses Authentifizierungsprotokoll auf einem eigenständigen Windows 2000-Server unterstützt wird. Der Wert 0 gibt an, dass der EAP nicht unterstützt wird. Der Standardwert ist 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Konstanter Wert | RolesSupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                                                                 |
| Beschreibung    | Gibt die verschiedenen Rollen an, die von EAP unterstützt werden. Dies gibt an, ob es auf einem Server oder client verwendet werden kann, ob es für RAS-Verbindungen (VPN) oder PEAP unterstützt wird. Standardmäßig wird die EAP-Methode in PEAP und EAP angezeigt. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Konstanter Wert | PerPolicyConfig |
|----------------|-----------------|
| type           | REG_DWORD      |
| Beschreibung    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Dieser Registrierungswert wird nicht verwendet.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Dieser Registrierungswert wird nicht verwendet.

