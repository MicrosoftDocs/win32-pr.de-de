---
description: Enthält ausführliche Informationen zu einer Schnittstelle, die für einen RPC-Client erforderlich ist.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: INTF_ENTRY Struktur (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527650"
---
# <a name="intf_entry-structure"></a>INTF- \_ Eintrags Struktur

\[**INTF \_ Der Eintrag** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

Enthält ausführliche Informationen zu einer Schnittstelle, die für einen RPC-Client erforderlich ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**wszguid**
</dt> <dd>

Ein Zeiger auf die GUID der Schnittstelle, die als Unicode-Zeichenfolge im folgenden Format dargestellt wird: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> <dt>

**wszdescr**
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die die Schnittstellen Beschreibung enthält, die vom drahtlos Konfigurations Dienst (wzcsvc) abgerufen wird.

</dd> <dt>

**dwcontext**
</dt> <dd>

Für die interne Verwendung reserviert.

</dd> <dt>

**ulmediastate**
</dt> <dd>

Der aktuelle NDIS-Medien Verbindungsstatus für die Schnittstelle. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                  | Bedeutung                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt> **Medien \_ Status \_ verbunden**</dt> <dt>1</dt> </dl>       | Das Medium ist verbunden.<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**Medien \_ Status \_ getrennt**</dt> <dt>0</dt> </dl> | Die Medien werden getrennt.<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**Medien \_ \_Unbekannter Status**</dt> <dt>-1</dt> </dl>               | Der Medien Status ist unbekannt.<br/> |



 

</dd> <dt>

**ulmediatype**
</dt> <dd>

Die NDIS-Medientypen, die derzeit von der NIC verwendet werden. Beim Abfragen ist der Wert dieses Members **NdisMedium802 \_ 3** , wie in der *ndispnp. h* -Header Datei definiert.

</dd> <dt>

**ulphysicalmediatype**
</dt> <dd>

Der NDIS-Medientyp für die-Schnittstelle. Beim Abfragen lautet der Wert dieses Members **ndisphysicalmedienwirelesslan** , wie in der *ndispnp. h* -Header Datei definiert.

</dd> <dt>

**ninframode**
</dt> <dd>

Der aktuelle 802,11-Infrastrukturmodus für die-Schnittstelle.

</dd> <dt>

**nauthmode**
</dt> <dd>

Der aktuelle 802,11-Authentifizierungsmodus für die-Schnittstelle.

In der folgenden Tabelle werden die möglichen Werte für den-Parameter basierend auf der in der Header Datei *ntddndis. h* definierten Enumeration für den **NDIS \_ 802 \_ 11- \_ authentifizierungmodus \_** angezeigt.



| Wert                                                                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11authmodeopen**</dt> <dt>1</dt> </dl>                         | IEEE 802,11 öffnen Sie die System Authentifizierung.<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11authmodeshared**</dt> <dt>2</dt> </dl>                 | Die freigegebene IEEE 802,11-Authentifizierung, bei der ein vorinstaltzter WEP-Schlüssel (Wired Equivalent Privacy) verwendet wird. <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11authmodeautoswitch**</dt> <dt>3</dt> </dl> | Automatischer switchmodus. Wenn Sie den Auto-Switch-Modus verwenden, versucht die drahtlos Netzwerkschnittstellenkarte (NIC) zuerst den freigegebenen Authentifizierungsmodus. Wenn der Modus "freigegeben" fehlschlägt, versucht die NIC, den offenen Authentifizierungsmodus zu verwenden <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11authmodewpa**</dt> <dt>4</dt> </dl>                             | Sicherheit des drahtlos geschützten Zugriffs (WPA). Die Authentifizierung erfolgt zwischen dem Supplicant-, Authenticator-und Authentifizierungsserver über IEEE 802.1 x. Verschlüsselungsschlüssel sind dynamisch und werden durch den Authentifizierungsprozess abgeleitet. <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11authmodewpapsk**</dt> <dt>5</dt> </dl>                 | WPA-Sicherheit mit einem vorinstallierten Schlüssel. Die Authentifizierung erfolgt zwischen dem Supplicant und Authentifikator über IEEE 802.1 x. Verschlüsselungsschlüssel sind dynamisch und werden über den vorinstallierten Schlüssel abgeleitet, der vom Supplicant und Authentifikator verwendet wird. <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11authmodewpanone**</dt> <dt>6</dt> </dl>             | WPA-Sicherheit. Die Authentifizierung erfolgt mithilfe eines vorinstallierten Schlüssels ohne IEEE 802.1 x-Authentifizierung. Verschlüsselungsschlüssel sind statisch und werden über den vorinstallierten Schlüssel abgeleitet. Dieser Modus gilt nur für Ad-hoc-Netzwerktypen. <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11authmodewpf2**</dt> <dt>7</dt> </dl>                         | WPA2-Sicherheit. Die Authentifizierung erfolgt zwischen dem Supplicant-, Authenticator-und Authentifizierungsserver über IEEE 802.1 x. Verschlüsselungsschlüssel sind dynamisch und werden durch den Authentifizierungsprozess abgeleitet. <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11authmodewpa2psk**</dt> <dt>8</dt> </dl>             | Gibt die WPA2-Sicherheit an. Die Authentifizierung erfolgt zwischen dem Supplicant und Authentifikator über IEEE 802 1X. Verschlüsselungsschlüssel sind dynamisch und werden über den vorinstallierten Schlüssel abgeleitet, der vom Supplicant und Authentifikator verwendet wird. <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11authmodemax**</dt> <dt>9</dt> </dl>                             | Der maximal mögliche Wert für den Enumerationswert des **NDIS \_ 802 \_ 11- \_ Authentifizierungs \_ Modus** . Dies ist kein gültiger Wert für den Authentifizierungsmodus. <br/>                                                                                        |



 

</dd> <dt>

**nwepstatus**
</dt> <dd>

Der aktuelle 802,11-Verschlüsselungs Modus für die-Schnittstelle.

</dd> <dt>

**dwctlflags**
</dt> <dd>

Ein Bitmasken Wert von steuerungflags, die angeben, wie wzcsvc auf der Schnittstelle funktioniert.

In der folgenden Tabelle werden die möglichen Bitwerte angezeigt.



| Wert                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**Intfctl \_ CM- \_ Maske**</dt> <dt>0x0007</dt> </dl>      | Eine Bitmaske für den Netzwerk Filter Modus. Die intfctl \_ cm \_ Mask-& dwctlflags ergeben einen Wert vom Typ NDIS \_ 802 \_ 11 \_ Network \_ Infrastructure. Der resultierende Wert gibt an, ob wzcsvc nur mit Infrastruktur Netzwerken, Ad-hoc-Netzwerken oder mit beiden Arten von Netzwerken verbunden ist.<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**Intfctl \_**</dt> <dt>0X8000</dt> aktiviert </dl>       | Gibt an, ob die Schnittstelle von wzcsvc konfiguriert werden soll.<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**Intfctl \_ Fallback**</dt> <dt>0x4000</dt> </dl>    | Wenn kein bevorzugtes Netzwerk verfügbar ist, gibt dieser Wert an, ob die NIC von wzcsvc automatisch so konfiguriert werden soll, dass Sie einem verfügbaren Netzwerk zugeordnet wird.<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **Intfctl \_ oidssupp**</dt> <dt>0x2000</dt> </dl> | Gibt an, ob der NIC-Treiber alle 802,11 OIDs unterstützt, die von wzcsvc benötigt werden.<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt> **Intfctl \_ volatile**</dt> <dt>0x1000</dt> </dl> | Gibt an, ob die Dienst Parameter für diese Schnittstelle in der Registrierung aufbewahrt werden sollen. <br/> Wenn dieser Wert festgelegt ist, sind diese Parameter flüchtig und sollten nicht in der Registrierung aufbewahrt werden.<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt> **Intfctl- \_ Richtlinie**</dt> <dt>0x0800</dt> </dl>       | Gibt an, ob die Dienst Parameter für diese Schnittstelle von einer Gruppenrichtlinie übermittelt werden.<br/> Wenn dieser Wert festgelegt ist, werden die Dienst Parameter über die Gruppenrichtlinie auf den lokalen Computer übermittelt.<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**Intfctl \_ 8021xsupp**</dt> <dt>0x1000</dt> </dl> | Gibt an, ob 802.1 x-Unterstützung aktiviert ist.<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwdynflags**
</dt> <dd>

Eine Bitmaske dynamischer Flags, die das dynamische (nicht persistente und nicht statische) Verhalten für die Schnittstelle steuern.

Diese Bits sind nützlich, um dynamische, temporäre Änderungen in der Art und Weise zu initiieren, in der wzcsvc auf die Schnittstelle angewendet wird. Keines dieser Bits wird in der Registrierung persistent gespeichert, sodass die Einstellungen einen Systemneustart oder eine Geräte-und Aktivierungs Sequenz nicht überstehen.

In der folgenden Tabelle werden die möglichen Bitwerte angezeigt.



| Wert                                                                                                                                                                                                                            | Bedeutung                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**Intfädyn \_ NOSCAN**</dt> <dt>0x00000001</dt> </dl> | Gibt an, dass wzcsvc nicht verlangen soll, dass die Schnittstelle eine aktive Überprüfung durchführt, sondern stattdessen die zwischengespeicherten Werte im NIC-Treiber verwendet.<br/> |



 

</dd> <dt>

**DW-Funktionen**
</dt> <dd>

Gibt die Treiberfunktionen an.



| Wert                                                                                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**Intfcap \_ Maximale Verschlüsselungs \_ \_ Maske**</dt> <dt>0x000000ff</dt> </dl> | Die unteren Reihenfolge dieser Member wird verwendet, um die maximale Verschlüsselung anzugeben, die unterstützt wird. Mögliche Werte sind einige der Enumerationswerte, die in der **NDIS \_ 802 \_ 11- \_ WEP- \_ Status** Struktur in der Header Datei *ntddndis. h* definiert sind, die in der Windows SDK enthalten ist.<br/> Der Ndis802 \_ 11verschlüsselungs1aktivierte Wert (2) gibt an, dass WEP unterstützt wird. TKIP und AES werden nicht unterstützt, und ein Übertragungs Schlüssel ist möglicherweise nicht verfügbar. <br/> Der Ndis802 \_ 11verschlüsselungs2aktivierte Wert (9) gibt an, dass TKIP und WEP unterstützt werden. AES wird nicht unterstützt, und es ist ein Übertragungs Schlüssel verfügbar. <br/> Der \_ Wert Ndis802 11verschlüsselungs3aktivierte (11) gibt an, dass AES, TKIP und WEP unterstützt werden und ein Übertragungs Schlüssel verfügbar ist. <br/> "Ndis802 \_ 11verschlüsselungnotsupported (8)" gibt an, dass der WEP-Schlüssel nicht unterstützt wird. <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**Intfcap \_ SSN**</dt> <dt>0x00000100</dt> </dl>                                       | Gibt die Unterstützung für Simple Secure Network (SSN) an, bei dem es sich um eine Teilmenge von 802.11 i handelt. <br/> Der Verschlüsselungsschlüssel wird von SSN regelmäßig geändert (im Gegensatz zum WEP-Standard (verkabelte äquivalente Datenschutz), in dem ein statischer Schlüssel verwendet wird. Damit SSN funktioniert, sollte die maximal unterstützte Verschlüsselung mindestens TKIP betragen. SSN wurde von einem Konsortium von Lieferanten in 2002 als Interims Ansatz entwickelt, um die drahtlose LAN-Sicherheit zu verbessern, während der IEEE 802.11 i-Standard abgeschlossen wurde.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**Intfcap \_ 80211i**</dt> <dt>0x00000200</dt> </dl>                              | Gibt die Unterstützung für den IEEE 802.11 i-Standard an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdniccapabilitäten**
</dt> <dd>

Eine Reihe von Funktionen für 802.11 i.

Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdniccapabili-** Daten zurück, wenn Sie mit dem INTF Functions-Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird. **\_** Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **pData** -Member der **\_ rohdatenstruktur** eine **INTF \_ 80211 \_** -Funktionsstruktur.

</dd> <dt>

**rdssid**
</dt> <dd>

Binärdaten, die die derzeit für die Schnittstelle konfigurierte 802,11 SSID enthalten.

Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdssid-** Daten zurück, wenn Sie mit dem **INTF \_ SSID** -Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird. Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** den **ssidlength** -Member einer **NDIS \_ 802 \_ 11 \_ SSID** -Struktur, und der **pData** -Member der **\_ rohdatenstruktur** enthält den **SSID-** Member einer **NDIS \_ 802 \_ 11 \_ SSID** -Struktur.

Die Struktur **NDIS \_ 802 \_ 11 \_ SSID** ist in der Header Datei *ntddndis. h* definiert.

</dd> <dt>

**rdbssid**
</dt> <dd>

Binärdaten, die die in der Schnittstelle konfigurierte 802,11 BSSID enthalten.

Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdbssid-** Daten zurück, wenn Sie mit dem **INTF \_ -BSSID-** Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird. Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** die Größe einer **NDIS \_ 802 \_ 11-Mac- \_ \_ Adress** Struktur, und der **pData** -Member der **\_ rohdatenstruktur** enthält die **NDIS \_ 802 \_ 11 Mac- \_ \_ Adress** Struktur.

Die **Mac- \_ \_ \_ \_ Adressstruktur von NDIS 802 11** ist in der Header Datei *ntddndis. h* definiert.

</dd> <dt>

**rdbssidlist**
</dt> <dd>

Binärdaten, die die Liste der BSSIDs enthalten, die zuletzt von wzcsvc abgerufen wurden.

Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdbssidlist** -Daten zurück, wenn Sie mit dem **INTF \_ bssidlist** -Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird. Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** die Länge des Puffers mit den zurückgegebenen Daten, und der **pData** -Member der **\_ rohdatenstruktur** enthält die **WZC \_ 802 \_ 11- \_ Konfigurations \_ Listen** Struktur.

</dd> <dt>

**rdstssidlist**
</dt> <dd>

Binärdaten, die die Liste der für diese Schnittstelle konfigurierten bevorzugten Netzwerke enthalten.

Die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion gibt **rdstssidlist** -Daten zurück, wenn Sie mit dem **INTF \_ preflist** -Flag aufgerufen wird, das im *dwInFlags* -Parameter übergeben wird. Wenn der Funktions Aufrufvorgang erfolgreich ist, enthält der **dwdatalen** -Member der **\_ rohdatenstruktur** die Länge des Puffers mit den zurückgegebenen Daten, und der **pData** -Member der **\_ rohdatenstruktur** enthält die **WZC \_ 802 \_ 11- \_ Konfigurations \_ Listen** Struktur.

Wenn eines der bevorzugten Netzwerke zurzeit verbunden ist, wird für den **dwctlflags** -Member der **WZC- \_ WLAN- \_ Konfigurations** Struktur für das Netzwerk das **wzcctl \_ Media \_ Connected** (0x0400) Bit festgelegt.

</dd> <dt>

**rdctrldata**
</dt> <dd>

Binäre Daten, die mit anderen steuerungflags verwendet werden, wenn zusätzliche Parameter für die Schnittstelle festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **INTF- \_ Eintrags** Struktur wird von den [**wzcqueryinterface**](wzcqueryinterface.md) -und [**wzkrefreshinterface**](wzcrefreshinterface.md) -Funktionen verwendet.

Die **\_ Rohdaten** Struktur ist wie folgt definiert:


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



Der *pData* -Member verweist auf Binärdaten. *Dwdatalen* gibt die Anzahl der Bytes an, auf die *pData* verweist.

> [!Note]  
> Die Header Datei " *wzcsapi. h* " ist im Windows SDK nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                       |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wzcenumschlag-Schnittstellen**](wzcenuminterfaces.md)
</dt> <dt>

[**Wzcqueryinterface**](wzcqueryinterface.md)
</dt> <dt>

[**Wzkrefreshinterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




