---
title: EAP-Methodenflags (Eaptypes.h)
description: Die EAP-Methodenflags werden innerhalb der Supplicant-, Authenticator- und Peerfunktionen verwendet, um das Verhalten einer EAP-Authentifizierungssitzung anzugeben.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91acce3b3829c947bfb6e705ad7e1f07b938a986bc6f6845a4c10a54b4f1992c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094410"
---
# <a name="eap-method-flags"></a>EAP-Methodenflags

Die EAP-Methodenflags werden innerhalb der Supplicant-, Authenticator- und Peerfunktionen verwendet, um das Verhalten einer EAP-Authentifizierungssitzung anzugeben.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP-FLAG \_ \_ reserviert1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP-FLAG \_ \_ NICHT \_ INTERAKTIV**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Zeigen Sie keine Benutzeroberfläche an.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**\_EAP-FLAGANMELDUNG \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Benutzerdaten wurden aus der Windows erhalten.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP-FLAG \_ \_ (VORSCHAUVERSION)**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Zeigen Sie die Benutzeroberfläche für Anmeldeinformationen vor der Authentifizierung an, auch wenn zwischengespeicherte Anmeldeinformationen vorhanden sind.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ FLAG \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP-FLAG \_ \_ FÜR \_ COMPUTERAUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Verwenden sie die Authentifizierung auf Computerebene. Wenn sie dieses Flag nicht festlegen, wird die Authentifizierung auf Benutzerebene verwendet.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP-FLAG \_ \_ FÜR \_ GASTZUGRIFF**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Gibt eine Anforderung zum Bereitstellen des Gastzugriffs an.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_EAP-FLAG \_ reserviert3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ FLAG \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP-FLAG \_ \_ "RESUME \_ FROM \_ HIBERNATE"**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Gibt an, dass dies der erste Aufruf ist, nachdem die Computeraktivität nach einem Zeitraum des Ruhezustands fortgesetzt wurde.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ FLAG \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_EAP-FLAG \_ reserviert6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP-FLAG \_ \_ FULL \_ AUTH**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Gibt an, dass Tunnelmethoden anstelle einer abgekürzten Version eine vollständige Authentifizierung durchführen sollen, z. B. [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP-FLAG \_ \_ BEVORZUGT \_ \_ ALT-ANMELDEINFORMATIONEN**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Gibt an, dass anmeldeinformationen, die an [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) übergeben werden, allen anderen Formen des Abrufens von Anmeldeinformationen vorgezogen werden, auch wenn konfigurationsdaten, die an die aktuelle Funktion übergeben werden, einen anderen Abrufmodus für Anmeldeinformationen anfordern.

> [!Note]  
> Dieses Flag wird nur von [**EapPeerBeginSession verwendet.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_EAP-FLAG \_ reserviert7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**ÄNDERUNG DES \_ INTEGRITÄTSZUSTANDS \_ DES EAP-PEERFLAGS \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Gibt an, dass die Ursache für die erneute Authentifizierung ein NAP-Rückruf [(Network Access Protection)](/windows/desktop/NAP/network-access-protection-start-page) ist. NAP hat die Authentifizierungssitzung initiiert, da sich der Integritätsstatus geändert hat. Dieses Flag darf nur gesendet werden, wenn diese Funktion von einem NAP-spezifischen [*NotificationHandler-Rückruf*](/previous-versions/windows/desktop/api) aufgerufen wird, der durch einen vorherigen Aufruf dieser Funktion bereitgestellt wurde.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_EAP-FLAG \_ \_ SUPRESS-BENUTZEROBERFLÄCHE**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Setzen Sie die Authentifizierung mit verfügbaren Informationen fort. Wenn die Authentifizierung nicht fortgesetzt werden kann, kann ein Fehler auftäusen.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP-FLAG \_ \_ VOR DER \_ ANMELDUNG**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Gibt an, dass EAPHost einmaliges Anmelden (Single Sign-On, SSO) bereitstellen soll. Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP-FLAG \_ \_ FÜR \_ BENUTZERAUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Gibt die Authentifizierung auf Benutzerebene für Legacymethoden an, die **EAP \_ FLAG MACHINE \_ \_ AUTH nicht festlegen können.**


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP-FLAG \_ \_ CONFG \_ READONLY**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Gibt an, dass die Konfiguration angezeigt, aber nicht aktualisiert werden kann.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP-FLAG \_ \_ reserviert8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

