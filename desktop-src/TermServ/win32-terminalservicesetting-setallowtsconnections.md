---
title: SetAllowTSConnections-Methode der Win32_TerminalServiceSetting-Klasse
description: Die SetAllowTSConnections-Methode ermöglicht oder verweigert neue Remotedesktopverbindungen. Diese Methode ändert die AllowTSConnections-Eigenschaft für die -Klasse entsprechend.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- SetAllowTSConnections-Methode Remotedesktopdienste
- SetAllowTSConnections-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting Klasse Remotedesktopdienste , SetAllowTSConnections-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f8e9be06a19599f578089fa979d7fd93a7bf457fcadf033ed0ab56fea4947f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127026"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>SetAllowTSConnections-Methode der Win32 \_ TerminalServiceSetting-Klasse

Die **SetAllowTSConnections-Methode** ermöglicht oder verweigert neue Remotedesktopverbindungen. Diese Methode ändert die **AllowTSConnections-Eigenschaft** für die -Klasse entsprechend.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AllowTSConnections* \[ In\]
</dt> <dd>

Gibt an, ob neue Remotedesktopverbindungen zulässig sind. Dies muss einer der folgenden Werte sein.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Neue Verbindungen sind nicht zulässig. Wenn der *ModifyFirewallException-Parameter* 1 ist, ist die Remotedesktop Firewallausnahme deaktiviert.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Neue Verbindungen sind zulässig. Wenn der *ModifyFirewallException-Parameter* 1 ist, wird die Remotedesktop Firewallausnahme aktiviert.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ In\]
</dt> <dd>

Gibt an, ob die Firewallausnahmeeinstellung für Remotedesktop in den vom *AllowTSConnections-Parameter* angegebenen Zustand geändert wird. Dies muss einer der folgenden Werte sein.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Ändern Sie die Firewallausnahmeeinstellung nicht.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Ändern Sie die Firewallausnahmeeinstellung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück. andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

