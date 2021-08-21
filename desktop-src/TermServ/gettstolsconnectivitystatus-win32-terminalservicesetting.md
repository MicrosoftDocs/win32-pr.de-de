---
title: GetTStoLSConnectivityStatus-Methode der Win32_TerminalServiceSetting Klasse
description: Bestimmt den Konnektivitätsstatus zwischen Remotedesktopdienste und einem Lizenzserver.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- GetTStoLSConnectivityStatus-Methode Remotedesktopdienste
- GetTStoLSConnectivityStatus-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , GetTStoLSConnectivityStatus-Methode
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
ms.openlocfilehash: ff79de8bc1740e659b8f0398c0fa84958c1bfcffda505f1a26322da442dcc19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059568"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>GetTStoLSConnectivityStatus-Methode der Win32 \_ TerminalServiceSetting-Klasse

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

*ServerName* \[ In\]
</dt> <dd>

Der Name des Lizenzservers, von dem der Konnektivitätsstatus überprüft werden soll.

</dd> <dt>

*TStoLSConnectivityStatus* \[ out\]
</dt> <dd>

Ein -Wert, der den Konnektivitätsstatus des Lizenzservers angibt. Dies kann einer der folgenden Werte sein.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_ CONNECTABLE \_ UNKNOWN** (0)


</dt> <dd>

Der Konnektivitätsstatus kann nicht bestimmt werden.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_ CONNECTABLE \_ VALID \_ WS08R2** (1)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008 R2-Lizenzserver herstellen.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_ CONNECTABLE \_ VALID \_ WS08** (2)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008-Lizenzserver herstellen.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_ CONNECTABLE \_ BETA \_ RTM \_ MISMATCH** (3)


</dt> <dd>

Remotedesktopdienste kann eine Verbindung mit dem Lizenzserver herstellen, aber auf einem der Server wird eine Betaversion des Betriebssystems ausgeführt.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_ CONNECTABLE \_ LOWER \_ VERSION** (4)


</dt> <dd>

Remotedesktopdienste kann eine Verbindung mit dem Lizenzserver herstellen, es besteht jedoch eine Inkompatibilität zwischen dem Lizenzserver und dem Remotedesktopdienste Hostserver.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_ CONNECTABLE \_ NOT \_ IN \_ TSCGROUP** (5)


</dt> <dd>

Die Sicherheitsgruppenrichtlinie ist auf dem Lizenzserver aktiviert, Remotedesktopdienste ist jedoch nicht Teil der Gruppenrichtlinie.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_ NICHT \_ VERBINDEND** (6)


</dt> <dd>

Remotedesktopdienste kann keine Verbindung mit dem Lizenzserver herstellen.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_ VERBINDUNGSFÄHIGE \_ UNBEKANNTE \_ GÜLTIGKEIT** (7)


</dt> <dd>

Mit dem Lizenzserver kann eine Verbindung hergestellt werden, aber die Gültigkeit der Verbindung kann nicht bestimmt werden.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_ \_VERBINDUNGSFÄHIG, \_ ABER ZUGRIFF \_ VERWEIGERT** (8)


</dt> <dd>

Remotedesktopdienste kann eine Verbindung mit dem Lizenzserver herstellen, aber das Benutzerkonto verfügt nicht über Administratorrechte auf dem Lizenzserver.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_ CONNECTABLE \_ VALID \_ WS08R2 \_ VDI** (9)


</dt> <dd>

Remotedesktopdienste können eine Verbindung mit dem Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) herstellen.

**Windows Server 2008 R2:** Dieser Wert wird nicht unterstützt, bevor Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_ \_VERBINDUNGSFÄHIGES FEATURE WIRD NICHT \_ \_ UNTERSTÜTZT** (10)


</dt> <dd>

Das Feature wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008 R2 mit SP1:** Dieser Wert wird vor der Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_ VERBINDUNGSFÄHIGE \_ GÜLTIGE \_ LS** (11)


</dt> <dd>

Der Lizenzserver ist gültig.

**Windows Server 2008 R2 und Windows Server 2008 R2 mit SP1:** Dieser Wert wird vor der Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





