---
description: Enthält Informationen zum 802.1 x-Verbindungsprofil, das zurzeit für die 802.1 x-Authentifizierung verwendet wird.
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
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356709"
---
# <a name="onex_connection_profile-structure"></a>Onex- \_ Verbindungs \_ Profil Struktur

Die **Onex- \_ Verbindungs \_ Profil** Struktur enthält Informationen zum 802.1 x-Verbindungsprofil, das zurzeit für die 802.1 x-Authentifizierung verwendet wird.

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

Die Version dieser **Onex- \_ Verbindungs \_ Profil** Struktur.

</dd> <dt>

**dwtotallen**
</dt> <dd>

Die Länge dieser **Onex- \_ Verbindungs \_ Profil** Struktur in Bytes.

</dd> <dt>

**fonexsupplicantflags**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwonexsupplicantflags** -Member enthält.

</dd> <dt>

**"losupplicantmode"**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **supplicantmode** -Member enthält.

</dd> <dt>

**"f"**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **authmode** -Member enthält.

</dd> <dt>

**"Gültigkeitsdauer"**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwheldperiod** -Member enthält.

</dd> <dt>

**Gültigkeitsdauer**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwauthperiod** -Member enthält.

</dd> <dt>

**Start Zeitraum**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwstartperiod** -Member enthält.

</dd> <dt>

**"f" starten**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwmaxstart** -Member enthält.

</dd> <dt>

**Fehler bei "f"**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwmaxauthfailure** -Member enthält.

</dd> <dt>

**"f"**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwnetworkauthtimeout** -Member enthält.

</dd> <dt>

**"f"-logondialoge**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **ballowlogondialogs** -Member enthält.

</dd> <dt>

**"f"**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **dwnetworkauthwithuitimeout** -Member enthält.

</dd> <dt>

**fuserbasedvlan**
</dt> <dd>

Gibt an, ob die **Onex- \_ Verbindungs \_ Profil** Struktur gültige Daten im **buserbasedvlan** -Member enthält.

</dd> <dt>

**dwonexsupplicantflags**
</dt> <dd>

Ein Satz von 802.1 x-Flags, die im Profil vorhanden sein können. Diese Flags sind für die interne Verwendung durch das 802.1 x-Authentifizierungs Modul reserviert.

</dd> <dt>

**supplicantmode**
</dt> <dd>

Das supplicantmode-Element im 802.1 x-Schema, das die Übertragungsmethode angibt, die für EAPOL-Start Nachrichten verwendet wird. Weitere Informationen finden Sie unter dem [**supplicantmode (Onex)-Element**](onexschema-supplicantmode-onex-element.md) im 802.1 x-Schema.



| Wert                                                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**Onexsupplicantmodeinhibittransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start-Nachrichten werden nicht übertragen. Nur für kabelgebundene LAN-profile gültig.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**Onexsupplicantmodelearn**</dt> <dt>1</dt> </dl>                                                         | Der Client legt fest, wann EAPOL-Start Pakete auf der Grundlage der Netzwerkfunktion gesendet werden sollen. EAPOL-Start Meldungen werden nur bei Bedarf gesendet. Nur für kabelgebundene LAN-profile gültig.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**Onexsupplicantmodecompliance**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start-Nachrichten werden gemäß 802.1 x übertragen. Gültig für Kabel-und Drahtlos-LAN-Profile.<br/>                                                             |



 

</dd> <dt>

**authmode**
</dt> <dd>

Das authmode-Element im 802.1 x-Schema, das den Typ der Anmelde Informationen angibt, die für die 802.1 x-Authentifizierung verwendet werden. Weitere Informationen finden Sie unter dem [**authmode-Element (Onex)**](onexschema-authmode-onex-element.md) im 802.1 x-Schema.



| Wert                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**Onexauthmodemachineoruser**</dt> <dt>0</dt> </dl> | Verwenden Sie Computer-oder Benutzer Anmelde Informationen. Wenn ein Benutzer angemeldet ist, werden die Anmelde Informationen des Benutzers zur Authentifizierung verwendet. Wenn kein Benutzer angemeldet ist, werden Computer Anmelde Informationen verwendet.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**Onexauthmodemachineonly**</dt> <dt>1</dt> </dl>         | Verwenden Sie nur Computer Anmelde Informationen.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**Onexauthmudeuseronly**</dt> <dt>2</dt> </dl>                     | Nur Benutzer Anmelde Informationen verwenden.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**Onexauthmodeguest**</dt> <dt>3</dt> </dl>                                 | Nur Gast Anmelde Informationen (leer) verwenden.<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**Onexauthmodeunspezifiziert**</dt> <dt>4</dt> </dl>         | Die zu verwendenden Anmelde Informationen wurden nicht angegeben.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwheldperiod**
</dt> <dd>

Das heldperiod-Element im 802.1 x-Schema, das die Zeitdauer in Sekunden angibt, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht. Weitere Informationen finden Sie unter dem [**heldperiod-Element (Onex)**](onexschema-heldperiod-onex-element.md) im 802.1 x-Schema.

</dd> <dt>

**dwauthperiod**
</dt> <dd>

Das authperiod-Element im 802.1 x-Schema, das die maximale Zeitspanne (in Sekunden) angibt, in der ein Client auf eine Antwort vom Authentifikator wartet. Wenn innerhalb des angegebenen Zeitraums keine Antwort empfangen wird, geht der Client davon aus, dass im Netzwerk kein Authentifikator vorhanden ist. Weitere Informationen finden Sie unter dem [**authperiod-Element (Onex)**](onexschema-authperiod-onex-element.md) im 802.1 x-Schema.

</dd> <dt>

**dwstartperiod**
</dt> <dd>

Das startperiod-Element im 802.1 x-Schema, das angibt, wie lange (in Sekunden) gewartet werden soll, bevor eine EAPOL-Start gesendet wird. Eine EAPOL-Start Nachricht wird gesendet, um den 802.1 x-Authentifizierungsprozess zu starten. Weitere Informationen finden Sie unter dem [**startperiod-Element (Onex)**](onexschema-startperiod-onex-element.md) im 802.1 x-Schema.

</dd> <dt>

**dwmaxstart**
</dt> <dd>

Das maxstart-Element im 802.1 x-Schema, das die maximale Anzahl von EAPOL-Start gesendeten Nachrichten angibt. Nachdem die maximale Anzahl von EAPOL-Start-Nachrichten gesendet wurde, nimmt der Client an, dass im Netzwerk kein Authentifikator vorhanden ist. Weitere Informationen finden Sie unter dem [**maxstart (Onex)-Element**](onexschema-maxstart-onex-element.md) im 802.1 x-Schema.

</dd> <dt>

**dwmaxauthfailure**
</dt> <dd>

Das maxauthfailure-Element im 802.1 x-Schema, das die maximale Anzahl von Authentifizierungs Fehlern angibt, die für einen Satz von Anmelde Informationen zulässig sind. Weitere Informationen finden Sie unter dem [**maxauthfailure (Onex)**](onexschema-maxauthfailures-onex-element.md) -Element im 802.1 x-Schema.

</dd> <dt>

**dwnetworkauthtimeout**
</dt> <dd>

Die Zeit in Sekunden, für die auf den Abschluss der 802.1 x-Authentifizierung gewartet werden soll, bevor die normale Anmeldung erfolgt. Dieser Wert wird in Szenarien mit einmaligem Anmelden (Single Sign-on, SSO) verwendet. Der Standardwert ist 10 Sekunden in einem 802.1 x-Profil. Weitere Informationen finden Sie unter dem [**MaxDelay-Element (SingleSignOn)**](onexschema-maxdelay-singlesignon-element.md) im 802.1 x-Schema.

</dd> <dt>

**dwnetworkauthwithuitimeout**
</dt> <dd>

Die maximale Dauer (in Sekunden), die auf eine Verbindung gewartet werden soll, falls ein Benutzeroberflächen Dialogfeld, das eine Benutzereingabe erfordert, während des einmaligen Anmeldens pro Anmeldung angezeigt wird.

Unter Windows Vista mit SP1 und höher ist dieser Wert in 10 Minuten hart codiert und kann nicht konfiguriert werden. In Windows Vista Release to Manufacturing ist dieser Wert standardmäßig auf 60 Sekunden in einem 802.1 x-Profil festgelegt und wurde vom Element **maxdelaywithadditionaldialoge** im Schema gesteuert.

Unter Windows Vista mit SP1 und höher wird das **maxdelaywithadditionaldialogs** -Element im 802.1 x-Schema ignoriert und als veraltet markiert.

</dd> <dt>

**ballowlogondialogfelder**
</dt> <dd>

Ein-Wert, der angibt, ob EAP-Dialoge bei Verwendung des einmaligen Anmeldens von SSO angezeigt werden dürfen. Weitere Informationen finden Sie unter dem **allowadditionaldialogs** -Element im 802.1 x-Schema.

</dd> <dt>

**buserbasedvlan**
</dt> <dd>

Das userbasedvirtuallan-Element im 802.1 x-Schema, das angibt, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird. Einige Netzwerk Zugriffs Server-Geräte (NAS) ändern das VLAN, nachdem sich ein Benutzer authentifiziert hat. Wenn userbasedvirtuallan den Wert true hat, kann der NAS das VLAN eines Geräts ändern, nachdem sich ein Benutzer authentifiziert hat. Weitere Informationen finden Sie unter dem [**userbasedvirtuallan (SingleSignOn)-Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) im 802.1 x-Schema.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Onex- \_ Verbindungs \_ Profil** Struktur wird vom 802.1 x-Modul verwendet, eine neue drahtlos Konfigurationskomponente, die unter Windows Vista und höher unterstützt wird.

Die [**Onex- \_ Ergebnis \_ Aktualisierungs \_ Daten**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) enthalten Informationen zu einer Statusänderung in der 802.1 x-Authentifizierung. Die **Datenstruktur der Onex- \_ Ergebnis \_ \_ Aktualisierung** wird zurückgegeben, wenn der **notificationsource** -Member der [**WLAN- \_ Benachrichtigungs \_ Daten**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) Struktur die **WLAN- \_ Benachrichtigungs \_ Quelle \_ Onex** und der **notificationcode** -Member der **WLAN- \_ Benachrichtigungs \_ Daten** Struktur für die empfangene Benachrichtigung **onexnotificationtyperesultupdate** ist. Für diese Benachrichtigung verweist der **pData** -Member der **WLAN- \_ Benachrichtigungs \_ Daten** Struktur auf eine Datenstruktur des **Onex- \_ Ergebnis \_ Updates \_** , die Informationen über die 802.1 x-Authentifizierungs Statusänderung enthält.

Wenn das Element " **fonexauthparser** " in der Datenstruktur der [**Onex- \_ Ergebnis \_ Aktualisierung \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) festgelegt ist, enthält das **authparameams** -Element der Datenstruktur des **Onex- \_ Ergebnis \_ \_ Updates** eine [**Onex-Variablen- \_ \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) -Struktur mit einer eingebetteten [**Onex \_ auth \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) -Parameter Struktur, beginnend beim **dwOffset** -Member des **Onex- \_ Variablen- \_ BLOB**. Der **onexconfiguration profile** -Member der **Onex \_ auth \_** -Parameter Struktur enthält eine **Onex- \_ Variablen- \_ BLOB** -Struktur mit einer eingebetteten **Onex- \_ Verbindungs \_ Profil** Struktur, beginnend beim **dwOffset** -Member des **Onex- \_ \_ variablenblobs**.

Die **Onex- \_ Verbindungs \_ Profil** Struktur ist nicht in einer öffentlichen Header Datei definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zur ACM-Architektur](about-the-acm-architecture.md)
</dt> <dt>

[Onex-Schema](onexschema-schema.md)
</dt> <dt>

[**authmode-Element (Onex)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**authperiod-Element (Onex)**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**heldperiod-Element (Onex)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxauthfailure (Onex)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**maxstart (Onex)-Element**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**startperiod (Onex)-Element**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**supplicantmode-Element (Onex)**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**userbasedvirtuallan (SingleSignOn)-Element**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**Onex \_ auth-Parameter \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**Onex \_ - \_ Benachrichtigungstyp**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**Onex- \_ Ergebnis \_ Aktualisierungs \_ Daten**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**Onex-Schema Element**](onexschema-onex-element.md)
</dt> <dt>

[**Onex \_ - \_ variablenblob**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**WLAN- \_ Benachrichtigungs \_ Daten**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**Wlanregisternotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
