---
description: Enthält Informationen zum 802.1X-Verbindungsprofil, das derzeit für die 802.1X-Authentifizierung verwendet wird.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: ONEX_CONNECTION_PROFILE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500e714b6f0728104987f53ff0a8c0e7083c1af5996679a78a986b5674d54514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684890"
---
# <a name="onex_connection_profile-structure"></a>ONEX \_ CONNECTION \_ PROFILE-Struktur

Die **ONEX \_ CONNECTION \_ PROFILE-Struktur** enthält Informationen zum 802.1X-Verbindungsprofil, das derzeit für die 802.1X-Authentifizierung verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Die Version dieser **ONEX \_ CONNECTION \_ PROFILE-Struktur.**

</dd> <dt>

**dwTotalLen**
</dt> <dd>

Die Länge dieser **ONEX \_ CONNECTION \_ PROFILE-Struktur** in Bytes.

</dd> <dt>

**fOneXSupplimultiFlags**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwOneXSuppli csvFlags-Member** enthält.

</dd> <dt>

**fsupplilvmode**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **suppli csvMode-Member** enthält.

</dd> <dt>

**modusthMode**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **authMode-Member** enthält.

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwHeldPeriod-Member** enthält.

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwAuthPeriod-Member** enthält.

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwStartPeriod-Member** enthält.

</dd> <dt>

**fMaxStart**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwMaxStart-Member** enthält.

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwMaxAuthFailures-Member** enthält.

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwNetworkAuthTimeout-Member** enthält.

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **bAllowLogonDialogs-Member** enthält.

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **dwNetworkAuthWithUITimeout-Member** enthält.

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Gibt an, ob die **ONEX \_ CONNECTION \_ PROFILE-Struktur** gültige Daten im **bUserBasedVLan-Member** enthält.

</dd> <dt>

**dwOneXSupplimultiFlags**
</dt> <dd>

Ein Satz von 802.1X-Flags, die im Profil vorhanden sein können. Diese Flags sind für die interne Verwendung durch das 802.1X-Authentifizierungsmodul reserviert.

</dd> <dt>

**suppli übermode**
</dt> <dd>

Das suppliproxyMode-Element im 802.1X-Schema, das die für EAPOL-Start Nachrichten verwendete Übertragungsmethode angibt. Weitere Informationen finden Sie unter dem [**supplimultiMode -Element (OneX)**](onexschema-supplicantmode-onex-element.md) im 802.1X-Schema.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSuppliproxyModeInhibitTransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start Nachrichten werden nicht übertragen. Nur für Kabel-LAN-Profile gültig.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSuppliproxyModeLearn**</dt> <dt>1</dt> </dl>                                                         | Der Client bestimmt basierend auf der Netzwerkfunktion, wann EAPOL-Start Pakete gesendet werden sollen. EAPOL-Start Nachrichten werden nur bei Bedarf gesendet. Nur für Kabel-LAN-Profile gültig.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSuppliproxyModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start Nachrichten werden gemäß 802.1X übertragen. Gültig sowohl für Kabel- als auch für Wlan-Profile.<br/>                                                             |



 

</dd> <dt>

**authMode**
</dt> <dd>

Das authMode-Element im 802.1X-Schema, das den Typ der für die 802.1X-Authentifizierung verwendeten Anmeldeinformationen angibt. Weitere Informationen finden Sie unter dem [**authMode -Element (OneX)**](onexschema-authmode-onex-element.md) im 802.1X-Schema.



| Wert                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Verwenden Sie Computer- oder Benutzeranmeldeinformationen. Wenn ein Benutzer angemeldet ist, werden die Anmeldeinformationen des Benutzers für die Authentifizierung verwendet. Wenn kein Benutzer angemeldet ist, werden Computeranmeldeinformationen verwendet.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Verwenden Sie nur Computeranmeldeinformationen.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Verwenden Sie nur Benutzeranmeldeinformationen.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Verwenden Sie nur Gastanmeldeinformationen (leer).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | Die zu verwendenden Anmeldeinformationen werden nicht angegeben.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

Das heldPeriod-Element im 802.1X-Schema, das die Zeitspanne in Sekunden angibt, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungsversuch nicht erneut versucht. Weitere Informationen finden Sie unter dem [**heldPeriod (OneX)-Element**](onexschema-heldperiod-onex-element.md) im 802.1X-Schema.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

Das authPeriod-Element im 802.1X-Schema, das die maximale Zeitdauer in Sekunden angibt, in der ein Client auf eine Antwort vom Authentifikator wartet. Wenn innerhalb des angegebenen Zeitraums keine Antwort empfangen wird, geht der Client davon aus, dass im Netzwerk kein Authentifikator vorhanden ist. Weitere Informationen finden Sie unter dem [**authPeriod (OneX)-Element**](onexschema-authperiod-onex-element.md) im 802.1X-Schema.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

Das startPeriod-Element im 802.1X-Schema, das die Wartezeit in Sekunden angibt, bevor ein EAPOL-Start gesendet wird. Eine EAPOL-Start Nachricht wird gesendet, um den 802.1X-Authentifizierungsprozess zu starten. Weitere Informationen finden Sie unter dem [**element startPeriod (OneX)**](onexschema-startperiod-onex-element.md) im 802.1X-Schema.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

Das maxStart-Element im 802.1X-Schema, das die maximale Anzahl der gesendeten EAPOL-Start Nachrichten angibt. Nachdem die maximale Anzahl von EAPOL-Start Nachrichten gesendet wurde, geht der Client davon aus, dass im Netzwerk kein Authentifikator vorhanden ist. Weitere Informationen finden Sie unter dem [**maxStart (OneX)-Element**](onexschema-maxstart-onex-element.md) im 802.1X-Schema.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

Das maxAuthFailures-Element im 802.1X-Schema, das die maximale Anzahl von Authentifizierungsfehlern angibt, die für einen Satz von Anmeldeinformationen zulässig sind. Weitere Informationen finden Sie im [**MaxAuthFailures -Element (OneX)**](onexschema-maxauthfailures-onex-element.md) im 802.1X-Schema.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

Die Zeit in Sekunden, die auf den Abschluss der 802.1X-Authentifizierung gewartet werden soll, bevor die normale Anmeldung fortgesetzt wird. Dieser Wert wird in Szenarien mit einmaligem Anmelden (Single Signon, SSO) verwendet. Dieser Wert ist in einem 802.1X-Profil standardmäßig auf 10 Sekunden eingestellt. Weitere Informationen finden Sie unter dem [**maxDelay (singleSignOn)-Element**](onexschema-maxdelay-singlesignon-element.md) im 802.1X-Schema.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

Die maximale Dauer in Sekunden für das Warten auf eine Verbindung, falls während des einmaligen Anmeldens ein Dialogfeld für die Benutzeroberfläche angezeigt wird, für das Benutzereingaben erforderlich sind.

Auf Windows Vista mit SP1 und höher ist dieser Wert auf 10 Minuten hartcodiert und kann nicht konfiguriert werden. Bei Windows Vista Release to Manufacturing beträgt dieser Wert standardmäßig 60 Sekunden in einem 802.1X-Profil und wurde vom **maxDelayWithAdditionalDialogs-Element** im Schema gesteuert.

Auf Windows Vista mit SP1 und höher wird das **maxDelayWithAdditionalDialogs-Element** im 802.1X-Schema ignoriert und veraltet.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Ein -Wert, der angibt, ob EAP-Dialoge angezeigt werden sollen, wenn einmaliges Anmelden vor der Anmeldung verwendet wird. Weitere Informationen finden Sie unter dem **allowAdditionalDialogs-Element** im 802.1X-Schema.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

Das userBasedVirtualLan-Element im 802.1X-Schema, das angibt, ob sich das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmeldeinformationen des Benutzers ändert. Einige NAS-Geräte (Network Access Server) ändern das VLAN, nachdem sich ein Benutzer authentifiziert hat. Wenn userBasedVirtualLan true ist, kann der NAS das VLAN eines Geräts ändern, nachdem sich ein Benutzer authentifiziert hat. Weitere Informationen finden Sie unter [**dem userBasedVirtualLan-Element (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) im 802.1X-Schema.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ONEX \_ CONNECTION \_ PROFILE-Struktur** wird vom 802.1X-Modul verwendet, einer neuen drahtlosen Konfigurationskomponente, die unter Windows Vista und höher unterstützt wird.

[**ONEX \_ RESULT UPDATE \_ \_ DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) enthält Informationen zu einer Statusänderung in die 802.1X-Authentifizierung. Die **ONEX \_ RESULT UPDATE \_ \_ DATA-Struktur** wird zurückgegeben, wenn das **NotificationSource-Mitglied** der [**WLAN NOTIFICATION \_ \_ DATA-Struktur**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) **WLAN NOTIFICATION SOURCE \_ \_ \_ ONEX** und das **NotificationCode-Member** der **WLAN NOTIFICATION \_ \_ DATA-Struktur** für die empfangene Benachrichtigung **OneXNotificationTypeResultUpdate** ist. Für diese Benachrichtigung verweist **das pData-Element** der **WLAN NOTIFICATION \_ \_ DATA-Struktur** auf eine **ONEX RESULT UPDATE \_ \_ \_ DATA-Struktur,** die Informationen zur Änderung des 802.1X-Authentifizierungsstatus enthält.

Wenn das **fOneXAuthParams-Member** in der [**ONEX \_ RESULT UPDATE \_ \_ DATA-Struktur**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) festgelegt ist, enthält das **authParams-Member** der **ONEX RESULT UPDATE \_ \_ \_ DATA-Struktur** eine [**ONEX \_ \_ VARIABLE-BLOB-Struktur**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) mit einer [**ONEX \_ \_ AUTH-PARAMS-Struktur,**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) die ab **dem dwOffset-Member** des **ONEX \_ VARIABLE-BLOB eingebettet \_ wird.** Das **oneXConnProfile-Element** der **ONEX \_ \_ AUTH-PARAMS-Struktur** enthält eine **ONEX \_ \_ VARIABLE-BLOB-Struktur** mit einer **ONEX \_ CONNECTION \_ PROFILE-Struktur,** die ab dem **dwOffset-Element** des ONEX VARIABLE BLOB eingebettet **\_ \_ ist.**

Die **ONEX \_ CONNECTION \_ PROFILE-Struktur** ist nicht in einer öffentlichen Headerdatei definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zur ACM-Architektur](about-the-acm-architecture.md)
</dt> <dt>

[OneX-Schema](onexschema-schema.md)
</dt> <dt>

[**authMode-Element (OneX)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**authPeriod (OneX)-Element**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**heldPeriod-Element (OneX)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**maxStart(OneX)-Element**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**startPeriod-Element (OneX)**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**supplicantMode(OneX)-Element**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**userBasedVirtualLan -Element (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**\_ \_ ONEX-AUTHENTIFIZIERUNGS-PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**\_ONEX-BENACHRICHTIGUNGSTYP \_**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**\_ \_ ONEX-ERGEBNISAKTUALISIERUNGSDATEN \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**OneX-Schemaelement**](onexschema-onex-element.md)
</dt> <dt>

[**ONEX \_ VARIABLE \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**\_WLAN-BENACHRICHTIGUNGSDATEN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WLANRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
