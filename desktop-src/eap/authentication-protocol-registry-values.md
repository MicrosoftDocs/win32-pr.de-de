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
# <a name="authentication-protocol-registry-values"></a>Registrierungs Werte für das Authentifizierungsprotokoll

Die Setup Software für die EAP-dll erstellt möglicherweise die folgenden Registrierungs Werte unter **&lt; eaptypeid &gt;**. Diese Registrierungs Werte werden in der Header Datei "raseapif. h" definiert. Die **RAS_EAP_VALUENAME_PATH** -und **RAS_EAP_VALUENAME_FRIENDLY_NAME** Werte sind erforderlich. Die Setup Software erstellt möglicherweise auch andere Schlüssel und Werte. Diese können vom Authentifizierungsprotokoll selbst verwendet werden. Weitere Informationen und ein Beispiel für die Registrierungs Konfiguration finden Sie unter [Beispiel für Registrierungs Werte](registry-values-example.md).

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
| type           | REG_EXPAND_SZ                    |
| BESCHREIBUNG    | Gibt den Pfad zur EAP-dll an. |

## <a name="ras_eap_valuename_friendly_name"></a>RAS_EAP_VALUENAME_FRIENDLY_NAME

| Konstanter Wert | FriendlyName                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_SZ                                                                                                                                                           |
| BESCHREIBUNG    | Gibt einen anzeigen Amen für das Authentifizierungsprotokoll an. Dieser Name wird in der Benutzeroberfläche der EAP-Anwendung sowohl für Einwähl-als auch für drahtlose Implementierungen angezeigt. |

## <a name="ras_eap_valuename_configui"></a>RAS_EAP_VALUENAME_CONFIGUI

| Konstanter Wert | Configuipath                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_EXPAND_SZ                                                                                                                   |
| BESCHREIBUNG    | Gibt den Pfad zu der dll an, die die Benutzeroberfläche für die Konfiguration auf dem Client implementiert, da diese Benutzeroberfläche ausschließlich für Client vorgesehen ist. |

## <a name="ras_eap_valuename_default_data"></a>RAS_EAP_VALUENAME_DEFAULT_DATA

| Konstanter Wert | ConfigData                                                            |
|----------------|-----------------------------------------------------------------------|
| type           | REG_BINARY                                                           |
| BESCHREIBUNG    | Gibt Standard Konfigurationsdaten für das Authentifizierungsprotokoll an. |

## <a name="ras_eap_valuename_require_configui"></a>RAS_EAP_VALUENAME_REQUIRE_CONFIGUI

| Konstanter Wert | Requirements configui                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                                                                               |
| BESCHREIBUNG    | Gibt an, ob der Benutzer Konfigurationsdaten in der Benutzeroberfläche der EAP-Client Anwendung bereitstellen muss. Wenn dieser Wert 1 ist, kann der Benutzer die Benutzeroberfläche der EAP-Client Anwendung nicht beenden, ohne Konfigurationsdaten bereitzustellen. Der Standardwert ist 0. |

## <a name="ras_eap_valuename_config_clsid"></a>RAS_EAP_VALUENAME_CONFIG_CLSID

| Konstanter Wert | Configclsid                                                   |
|----------------|---------------------------------------------------------------|
| type           | REG_SZ                                                       |
| BESCHREIBUNG    | Gibt die Klassen-ID der Konfigurations Benutzeroberfläche auf dem Server an. |

## <a name="ras_eap_valuename_identity"></a>RAS_EAP_VALUENAME_IDENTITY

| Konstanter Wert | Identitypath                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_EXPAND_SZ                                                                                                                        |
| BESCHREIBUNG    | Gibt den Pfad zu der dll an, die Funktionen implementiert, um die Benutzeridentität auf dem Client abzurufen, da diese Benutzeroberfläche nur für den Client bestimmt ist. |

## <a name="ras_eap_valuename_interactiveui"></a>RAS_EAP_VALUENAME_INTERACTIVEUI

| Konstanter Wert | Interactiveuipath                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_EXPAND_SZ                                                                                                                 |
| BESCHREIBUNG    | Gibt den Pfad zu der dll an, die die interaktive Benutzeroberfläche auf dem Client implementiert, da diese Benutzeroberfläche nur für den Client bestimmt ist. |

## <a name="ras_eap_valuename_invoke_namedlg"></a>RAS_EAP_VALUENAME_INVOKE_NAMEDLG

| Konstanter Wert | Invokeusernamedialog                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                             |
| BESCHREIBUNG    | Gibt an, ob RAS das Standard Dialogfeld für Windows NT/Windows 2000-Benutzername (Wert 1) oder [**raseapgetidentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (Wert 0) anzeigen soll. Der Standardwert ist 1. |

## <a name="ras_eap_valuename_invoke_pwddlg"></a>RAS_EAP_VALUENAME_INVOKE_PWDDLG

| Konstanter Wert | Invokepassworddialog                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                  |
| BESCHREIBUNG    | Gibt an, ob RAS das Standard Dialogfeld Windows NT/Windows 2000-Kennwort anzeigen soll. Wenn dieser Wert vorhanden ist und 0 ist, zeigt RAS das Kenn Wort Dialogfeld nicht an. Der Standardwert ist 1. |


## <a name="ras_eap_valuename_encryption"></a>RAS_EAP_VALUENAME_ENCRYPTION

| Konstanter Wert | Mppeer-Unterstützung                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                    |
| BESCHREIBUNG    | Wenn dieser Wert 1 ist, kann das Authentifizierungsprotokoll Schlüssel für den Microsoft-MPPE-Verschlüsselungs Stil (Point-to-Point Encryption, MPPE) generieren. Mögliche Werte sind 0 oder 1. Der Standardwert ist 0. |

## <a name="ras_eap_valuename_standalone_supported"></a>RAS_EAP_VALUENAME_STANDALONE_SUPPORTED

| Konstanter Wert | Standalonesupportiert                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                     |
| BESCHREIBUNG    | Gibt an, ob dieses Authentifizierungsprotokoll auf einem eigenständigen Windows 2000-Server unterstützt wird. Der Wert 0 gibt an, dass EAP nicht unterstützt wird. Der Standardwert ist 1. |

## <a name="ras_eap_valuename_roles_supported"></a>RAS_EAP_VALUENAME_ROLES_SUPPORTED

| Konstanter Wert | Rolessupported                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG_DWORD                                                                                                                                                                                                                                 |
| BESCHREIBUNG    | Gibt die verschiedenen Rollen an, die das EAP unterstützt. Dies gibt an, ob es auf einem Server oder Client verwendet werden kann, ob es für RAS-Verbindungen (VPN) oder PEAP unterstützt wird. Das Standardverhalten besteht darin, die EAP-Methode in PEAP und in EAP anzuzeigen. |

## <a name="ras_eap_valuename_per_policy_config"></a>RAS_EAP_VALUENAME_PER_POLICY_CONFIG

| Konstanter Wert | Perpolicyconfig |
|----------------|-----------------|
| type           | REG_DWORD      |
| BESCHREIBUNG    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a>RAS_EAP_VALUENAME_ISTUNNEL_METHOD

Dieser Registrierungs Wert wird nicht verwendet.

## <a name="ras_eap_valuename_filter_innermethods"></a>RAS_EAP_VALUENAME_FILTER_INNERMETHODS

Dieser Registrierungs Wert wird nicht verwendet.

