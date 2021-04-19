---
title: Extendeddisconnecationcode-Enumeration
description: Definiert erweiterte Informationen über den Grund für die Trennung der Verbindung.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Extendeddisconnecationcode-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345511"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a>Extendeddisconnecationcode-Enumeration

Definiert erweiterte Informationen über den Grund für die Trennung der Verbindung.

## <a name="syntax"></a>Syntax


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exdiscreasonnoinfo**
</dt> <dd>

Es sind keine zusätzlichen Informationen verfügbar.

</dd> <dt>

<span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exdiscreasonapiinitiateddisconnect**
</dt> <dd>

Eine Anwendung hat die Trennung der Verbindung initiiert.

</dd> <dt>

<span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exdiscreasonapiinitiatedlogoff**
</dt> <dd>

Eine Anwendung, die sich vom Client abgemeldet hat.

</dd> <dt>

<span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exdiscreasonserveridletimeout**
</dt> <dd>

Der Server wurde vom Server getrennt, da der Client für einen Zeitraum im Leerlauf war, der länger als der festgelegte Timeout Zeitraum ist.

</dd> <dt>

<span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exdiscreasonserverlogontimeout**
</dt> <dd>

Der Server hat den Client getrennt, da der Client den für die Verbindung vorgesehenen Zeitraum überschritten hat.

</dd> <dt>

<span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exdiscreasonreplacedbyotherconnection**
</dt> <dd>

Die Verbindung des Clients wurde durch eine andere Verbindung ersetzt.

</dd> <dt>

<span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exdiscreasonouto-Memory**
</dt> <dd>

Es ist kein Arbeitsspeicher verfügbar.

</dd> <dt>

<span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exdiscreasonserverdeniedconnection**
</dt> <dd>

Der Server hat die Verbindung verweigert.

</dd> <dt>

<span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exdiscreasonserverdeniedconnectionfps**
</dt> <dd>

Der Server hat die Verbindung aus Sicherheitsgründen verweigert.

</dd> <dt>

<span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exdiscreasonserverinsuffizientprivileges**
</dt> <dd>

Der Server hat die Verbindung aus Sicherheitsgründen verweigert.

</dd> <dt>

<span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exdiscreasonserverfreshkredsrequired**
</dt> <dd>

Es sind neue Anmelde Informationen erforderlich.

</dd> <dt>

<span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exdiscreasonrpcinitiateddisconnectbyuser**
</dt> <dd>

Die Benutzeraktivität hat die Verbindung initiiert.

</dd> <dt>

<span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exdiscreasonlogoffbyuser**
</dt> <dd>

Der Benutzer hat sich angemeldet und trennt die Sitzung.

</dd> <dt>

<span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exdiscreasonlicenseinternal**
</dt> <dd>

Interner Lizenzierungs Fehler.

</dd> <dt>

<span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exdiscreasonlicensenolicenseserver**
</dt> <dd>

Es war kein Lizenzserver verfügbar.

</dd> <dt>

<span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exdiscreasonlicensenolicense**
</dt> <dd>

Es war keine gültige Software Lizenz verfügbar.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exdiscreasonlicenseerrclientmsg**
</dt> <dd>

Der Remote Computer hat eine ungültige Lizenzierungs Nachricht erhalten.

</dd> <dt>

<span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exdiscreasonlicensehwiddoesntmatchlicense**
</dt> <dd>

Die Hardware-ID stimmt nicht mit der Hardware-ID, die in der Software Lizenz angegeben ist.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exdiscreasonlicenseerrclientlicense**
</dt> <dd>

Client Lizenz Fehler.

</dd> <dt>

<span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exdiscreasonlicensecantfinishprotocol**
</dt> <dd>

Während des Lizenzierungs Protokolls sind Netzwerkprobleme aufgetreten.

</dd> <dt>

<span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exdiscreasonlicenabclientendedprotocol**
</dt> <dd>

Der Client hat das Lizenzierungs Protokoll vorzeitig beendet.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exdiscreasonlicenseerrclientencryption**
</dt> <dd>

Eine Lizenzierungs Nachricht wurde falsch verschlüsselt.

</dd> <dt>

<span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exdiscreasonlicensecantupgradelicense**
</dt> <dd>

Die Client Zugriffslizenz des lokalen Computers konnte nicht aktualisiert oder erneuert werden.

</dd> <dt>

<span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exdiscreasonlicensenoremoteconnections**
</dt> <dd>

Der Remote Computer ist nicht für die Annahme von Remote Verbindungen lizenziert.

</dd> <dt>

<span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exdiscreasonlicensecreatinglicstoreaccdenied**
</dt> <dd>

Beim Erstellen eines Registrierungsschlüssels für den Lizenz Speicher wurde ein Fehler vom Typ "Zugriff verweigert" empfangen.

</dd> <dt>

<span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exdiscreasonrdpcinvalidanmelde Informationen**
</dt> <dd>

Ungültige Anmelde Informationen wurden gefunden.

</dd> <dt>

<span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exdiscreasonprotocolrangestart**
</dt> <dd>

Der Bereich interner Protokollfehler wird begonnen. Weitere Informationen finden Sie im Ereignisprotokoll des Servers.

</dd> <dt>

<span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exdiscreasonprotocolrangeend**
</dt> <dd>

Der Bereich interner Protokollfehler wird beendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Extendeddisconnecverrat**](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





