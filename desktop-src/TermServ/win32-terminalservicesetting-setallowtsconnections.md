---
title: Die Methode "-Methode" der Win32_TerminalServiceSetting-Klasse
description: Mit der Methode "*" können neue Remote Desktop Verbindungen zugelassen oder verweigert werden. Mit dieser Methode wird die allowtconnections-Eigenschaft für die-Klasse entsprechend geändert.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TerminalServiceSetting"
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, Methode "*"
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
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478834"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Die Methode "Setup-lowtconnections" der Win32- \_ Klasse "terminalservicesetts"

Mit **der Methode** "*" können neue Remote Desktop Verbindungen zugelassen oder verweigert werden. Mit dieser Methode wird die **allowtconnections** -Eigenschaft für die-Klasse entsprechend geändert.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Allow-connections* \[ in\]
</dt> <dd>

Gibt an, ob neue Remote Desktop Verbindungen zulässig sind. Dabei muss es sich um einen der folgenden Werte handeln:

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Neue Verbindungen sind nicht zulässig. Wenn der *modifyfirewallexception* -Parameter 1 ist, wird die Remotedesktop Firewallausnahme deaktiviert.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Neue Verbindungen sind zulässig. Wenn der *modifyfirewallexception* -Parameter 1 ist, wird die Remotedesktop Firewallausnahme aktiviert.

</dd> </dl> </dd> <dt>

*Modifyfirewallexception* \[ in\]
</dt> <dd>

Gibt an, ob die firewallausnahmeeinstellung für Remotedesktop in den durch den *allowzconnections* -Parameter angegebenen Zustand geändert wird. Dabei muss es sich um einen der folgenden Werte handeln:

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Ändern Sie die Einstellung für die Firewallausnahme nicht.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Ändern Sie die Einstellung für die Firewallausnahme.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

