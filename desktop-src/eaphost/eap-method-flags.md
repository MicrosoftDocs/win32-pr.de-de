---
title: EAP-methodenflags (eaptypes. h)
description: Die EAP-methodenflags werden innerhalb der Supplicant-, Authenticator-und Peer Funktionen verwendet, um das Verhalten einer EAP-Authentifizierungs Sitzung anzugeben.
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
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475021"
---
# <a name="eap-method-flags"></a>EAP-methodenflags

Die EAP-methodenflags werden innerhalb der Supplicant-, Authenticator-und Peer Funktionen verwendet, um das Verhalten einer EAP-Authentifizierungs Sitzung anzugeben.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP- \_ Flag \_ "reserved1"**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP- \_ Flag \_ nicht \_ interaktiv**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Zeigen Sie keine Benutzeroberfläche (UI) an.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP- \_ Flag- \_ Anmeldung**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Benutzerdaten wurden von der Windows-Anmeldung abgerufen.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP- \_ Flag ( \_ Vorschau)**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Anmelde Informationen-Benutzeroberfläche vor der Authentifizierung anzeigen, auch wenn zwischengespeicherte Anmelde Informationen vorhanden sind.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ Flag \_ "reserved2"**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP- \_ Flag für \_ Computer Authentifizierung \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Authentifizierung auf Computer Ebene verwenden; Wenn dieses Flag nicht festgelegt wird, wird die Authentifizierung auf Benutzerebene verwendet.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP- \_ Flag für \_ Gast \_ Zugriff**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Gibt eine Anforderung zum Bereitstellen des Gast Zugriffs an.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP- \_ Flag \_ "reserved3"**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ Flag \_ "reserved4"** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP-Flag fortsetzen \_ \_ \_ aus \_ Ruhezustand**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Gibt an, dass dies der erste Rückruf ist, nachdem die Computeraktivität von einem Ruhezustand wieder aufgenommen wurde.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ Flag \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP- \_ Flag \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP- \_ Flag für \_ vollständige \_ Authentifizierung**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Gibt an, dass Tunnel Methoden eine vollständige Authentifizierung anstelle einer abgekürzten Version durchführen sollen, z. b. eine [schnelle erneute Verbindungs Herstellung zwischen geschütztem EAP (PEAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10))


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP- \_ Flag \_ bevorzugt alt- \_ \_ Anmelde Informationen**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Gibt an, dass an [**eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) weiter gegebene Anmelde Informationen allen anderen Formen des Abrufs von Anmelde Informationen bevorzugt werden, auch wenn Konfigurationsdaten, die an die aktuelle Funktion weitergegeben werden, einen anderen Modus zum Abrufen von Anmelde Informationen anfordern.

> [!Note]  
> Dieses Flag wird nur von [**eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)verwendet.

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP- \_ Flag \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**Integritäts \_ \_ \_ \_ Status \_ Änderung des EAP-Peer Flags**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Gibt an, dass die erneute Authentifizierung ein NAP-Rückruf ( [Network Access Protection, Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page) ) ist. NAP hat die Authentifizierungs Sitzung initiiert, weil sich der Integritäts Status geändert hat. Dieses Flag muss nur gesendet werden, wenn diese Funktion von einem NAP-spezifischen [*notificationhandler*](/previous-versions/windows/desktop/api) -Rückruf aufgerufen wird, der von einem vorherigen Aufruf dieser Funktion bereitgestellt wird.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP- \_ Flag " \_ Supress" \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Setzen Sie die Authentifizierung mit verfügbaren Informationen fort. Wenn die Authentifizierung nicht fortgesetzt werden kann, schlägt fehl.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP- \_ Flag \_ vor der \_ Anmeldung**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Gibt an, dass EAPHost einmaliges Anmelden (Single-Sign-on, SSO) bereitstellen soll. Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP- \_ Flag \_ Benutzerauthentifizierung \_**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Gibt die Authentifizierung auf Benutzerebene für Legacy Methoden an, die die Authentifizierung des **EAP- \_ Flag \_ \_** nicht festlegen können.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP- \_ Flag " \_ confg" (schreibgeschützt) \_**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Gibt an, dass die Konfiguration angezeigt, aber nicht aktualisiert werden kann.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP- \_ Flag \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Darf nicht verwendet werden. Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

