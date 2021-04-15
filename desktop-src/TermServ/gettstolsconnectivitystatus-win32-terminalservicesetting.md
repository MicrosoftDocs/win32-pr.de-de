---
title: Gettstolsconnectivitystatus-Methode der Win32_TerminalServiceSetting-Klasse
description: Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Gettstolsconnectivitystatus-Methode Remotedesktopdienste
- Gettstolsconnectivitystatus-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, gettstolsconnectivitystatus-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477448"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Gettstolsconnectivitystatus-Methode der Win32 \_ terminalservicesetts-Klasse

Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.

## <a name="syntax"></a>Syntax


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* \[ in\]
</dt> <dd>

Der Name des Lizenzservers, von dem der Konnektivitätsstatus überprüft werden soll.

</dd> <dt>

*Tstolsconnectivitystatus* \[ vorgenommen\]
</dt> <dd>

Ein-Wert, der den Konnektivitätsstatus des Lizenzservers angibt. Dies kann einer der folgenden Werte sein:

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ Verbindungstabelle \_ unbekannt** (0)


</dt> <dd>

Der Konnektivitätsstatus kann nicht bestimmt werden.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ Connectable \_ valid \_ WS08R2** (1)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008 R2-Lizenz Server herstellen.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ Connectable \_ valid \_ WS08** (2)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008-Lizenz Server herstellen.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ Verbindungsfehler bei der Connectable- \_ Beta- \_ RTM \_** (3)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Lizenzserver herstellen, aber auf einem der Server wird eine Beta Version des Betriebssystems ausgeführt.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ Verbindungstabelle, \_ niedrigere \_ Version** (4)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Lizenzserver herstellen, aber es besteht eine Inkompatibilität zwischen dem Lizenzserver und dem Remotedesktopdienste Host Server.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ Connectable \_ nicht \_ in \_ tscgroup** (5)


</dt> <dd>

Die Sicherheitsgruppen Richtlinie ist auf dem Lizenzserver aktiviert, Remotedesktopdienste jedoch nicht Teil der Gruppenrichtlinie ist.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ Nicht \_ Connectable** (6)


</dt> <dd>

Remotedesktopdienste kann keine Verbindung mit dem Lizenzserver herstellen.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ Verbindungs fähige \_ unbekannte \_ Gültigkeit** (7)


</dt> <dd>

Der Lizenzserver kann mit verbunden werden, die Gültigkeit der Verbindung kann jedoch nicht bestimmt werden.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ Connectable, \_ aber \_ Zugriff \_ verweigert** (8)


</dt> <dd>

Remotedesktopdienste kann eine Verbindung mit dem Lizenzserver herstellen, aber das Benutzerkonto verfügt nicht über Administratorrechte auf dem Lizenzserver.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ Connectable \_ valid \_ WS08R2 \_ VDI** (9)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI)-Server herstellen.

**Windows Server 2008 R2:** Dieser Wert wird vor Windows Server 2012 nicht unterstützt.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ Die Connectable- \_ Funktion \_ \_ wird nicht unterstützt** (10)


</dt> <dd>

Das Feature wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008 R2 mit SP1:** Dieser Wert wird vor Windows Server 2012 nicht unterstützt.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ Verbindungs fähige \_ gültige \_ ls** (11)


</dt> <dd>

Der Lizenzserver ist gültig.

**Windows Server 2008 R2 und Windows Server 2008 R2 mit SP1:** Dieser Wert wird vor Windows Server 2012 nicht unterstützt.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





