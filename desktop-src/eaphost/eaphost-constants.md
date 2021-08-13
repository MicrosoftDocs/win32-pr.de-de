---
title: EAPHost-Konstanten (Eaptypes.h)
description: Zeigen Sie eine Liste der EAPHost-Konstanten (Eaptypes.h) an, die von EAPHost-Methoden verwendet werden, und sehen Sie sich die Anforderungen für deren Verwendung an.
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab336b147557722f1bec72bfe662b12599a64ee1622b31bdad6a92a05af6d92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119483010"
---
# <a name="eaphost-constants"></a>EAPHost-Konstanten

Die von EAPHost-Methoden verwendeten Konstanten.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**EAP \_ INTERACTIVE \_ UI \_ DATA \_ VERSION**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Die Version der interaktiven EAP-Benutzeroberflächendaten.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_EAP-ANMELDEINFORMATIONSVERSION \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Die Version der vom Benutzer bereitgestellten EAP-Anmeldeinformationen.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**\_ \_ EAPHOST-PEER-API-VERSION \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Die Version der EAPHost-Peer-API.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_ \_ ZERTIFIKATHASHLÄNGE**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Länge des SHA1-Hashs des Zertifikats.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**MAXIMALE \_ LÄNGE DES \_ EINGABEFELDS FÜR \_ DIE \_ EAP-KONFIGURATION \_**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Gibt die maximal unterstützte Länge eines Eingabefelds an.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**MAXIMALE \_ LÄNGE DES \_ EAP-EINGABEFELDWERTS \_ \_ FÜR DIE \_ \_ KONFIGURATION**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Gibt die maximal unterstützte Länge eines Eingabefelds an.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**EAP \_ UI \_ INPUT \_ FIELD \_ PROPS \_ DEFAULT**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista mit SP1 oder höher: Stellt den Standardeigenschaftswert für Eingabefeldeinträge dar, die auf der Benutzeroberfläche angezeigt werden.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**EAP \_ CONFIG \_ INPUT \_ FIELD \_ PROPS \_ DEFAULT**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Stellt den Standardeigenschaftswert für Konfigurationseingabefeldeinträge dar, die auf der Benutzeroberfläche angezeigt werden.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**EAP \_ UI \_ INPUT \_ FIELD \_ PROPS \_ NON \_ DISPLAYABLE**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista mit SP1 oder höher: Gibt an, dass Eingabefeldeinträge nicht auf der Benutzeroberfläche angezeigt werden (z. B. ein Kennwort oder eine PIN-Nummer).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**\_EAP-KONFIGURATIONSEINGABEFELD \_ \_ \_ PROPS \_ NON \_ DISPLAYABLE**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Gibt an, dass Eingabefeldeinträge für die Konfiguration nicht auf der Benutzeroberfläche angezeigt werden (z. B. ein Kennwort oder eine PIN-Nummer).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**EAP \_ UI \_ INPUT \_ FIELD \_ PROPS \_ NON \_ PERSIST**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista mit SP1 oder höher: Gibt an, dass die EAP-Methode die Felddaten nicht zwischenspeichert. der Supplicant muss die Felddaten für das Roaming zwischenspeichern.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**EAP \_ UI \_ INPUT \_ FIELD \_ PROPS \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista mit SP1 oder höher: Gibt an, dass das Eingabefeld schreibgeschützt ist und nicht bearbeitet werden kann.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Role | Unterstützte Mindestversion des Betriebssystems |
|------|------------------------------|
| Client<br/> | \[Windows 8 Nur Desktop-Apps\]<br/> |
| Server<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/> |



 

 





