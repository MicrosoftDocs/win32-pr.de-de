---
title: EAPHost-Konstanten (eaptypes. h)
description: Anzeigen einer Liste von EAPHost-Konstanten (eaptypes. h), die von EAPHost-Methoden verwendet werden, und Anzeigen der Anforderungen für deren Verwendung.
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
ms.openlocfilehash: 84704e59ed43466c47435f4804cb4dedc9c3a92d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391000"
---
# <a name="eaphost-constants"></a>EAPHost-Konstanten

Die von EAPHost-Methoden verwendeten Konstanten.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**interaktive EAP- \_ \_ UI- \_ Daten \_ Version**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Die Version der interaktiven EAP-UI-Daten.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**EAP-Anmelde Informations \_ \_ Version**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Die Version der EAP-Anmelde Informationen, die der Benutzer bereitgestellt hat.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**EAPHost- \_ Peer- \_ API- \_ Version**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Die Version der EAPHost-Peer-API.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**Zertifikat \_ Hash \_ Länge**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Länge des SHA1-Hashs des Zertifikats.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**maximale \_ Länge der EAP- \_ Konfigurations \_ Eingabe \_ Felder \_**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Gibt die maximal unterstützte Länge eines Eingabe Felds an.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**maximale \_ Länge des Werts für die EAP- \_ Konfigurations \_ Eingabe \_ Felder \_ \_**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Gibt die maximal unterstützte Länge eines Eingabe Felds an.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**Standardeigenschaften der EAP-Benutzeroberflächen- \_ \_ Eingabe \_ Felder \_ \_**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista mit SP1 oder höher: stellt den Standard Eigenschafts Wert für Eingabefeld Einträge dar, die auf der Benutzeroberfläche angezeigt werden.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**Standardeigenschaften der EAP- \_ Konfigurations \_ Eingabe \_ Felder \_ \_**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Stellt den Standard Eigenschafts Wert für Konfigurations Eingabefeld Einträge dar, die auf der Benutzeroberfläche angezeigt werden.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**Eingabefeld Eigenschaften für EAP- \_ Benutzeroberfläche \_ \_ \_ \_ nicht \_ anzeigbar**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista mit SP1 oder höher: gibt an, dass Eingabefeld Einträge nicht in der Benutzeroberfläche angezeigt werden (z. b. ein Kennwort oder eine PIN-Nummer).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**die Eigenschaften der EAP- \_ Konfigurations \_ Eingabe \_ Felder sind \_ \_ nicht \_ anzeigbar.**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Gibt an, dass die Einträge der Konfigurations Eingabefelder nicht in der Benutzeroberfläche angezeigt werden (z. b. ein Kennwort oder eine PIN-Nummer).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**EAP-Benutzeroberflächen- \_ \_ Eingabe \_ Feldeigenschaften \_ \_ nicht \_ persistent speichern**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista mit SP1 oder höher: gibt an, dass die EAP-Methode die Felddaten nicht zwischenspeichert. der Supplicant muss die Felddaten für das Roaming Zwischenspeichern.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**Eingabefeld Eigenschaften für EAP- \_ Benutzeroberfläche schreibgeschützt \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista mit SP1 oder höher: gibt an, dass das Eingabefeld schreibgeschützt ist und nicht bearbeitet werden kann.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstützte Betriebssystemversion |
|------|------------------------------|
| Client<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/> |
| Server<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/> |



 

 





