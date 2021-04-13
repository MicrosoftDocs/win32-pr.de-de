---
title: Setuserauthenticationrequired-Methode der Win32_TSGeneralSetting-Klasse
description: Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit authentifiziert werden müssen, indem der Wert der UserAuthenticationRequired-Eigenschaft festgelegt wird.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Setuserauthenticationrequired-Methode Remotedesktopdienste
- Setuserauthenticationrequired-Methode Remotedesktopdienste, Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste, setuserauthenticationrequired-Methode
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341128"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a>Setuserauthenticationrequired-Methode der Win32- \_ Klasse "zgeneralsetting"

Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit authentifiziert werden müssen, indem der Wert der **UserAuthenticationRequired** -Eigenschaft in der Win32-Klasse " [**\_ tgeneralsetting**](win32-tsgeneralsetting.md) " festgelegt wird. Wenn **true**, d. h. aktiviert, erfordert **UserAuthenticationRequired** eine Benutzerauthentifizierung zur Verbindungszeit, um den Server Schutz vor Netzwerk Angriffen zu erhöhen. Nur Remotedesktopprotokoll (RDP)-Clients, die RDP-Version 6,0 oder höher unterstützen, können eine Verbindung herstellen. Um Unterbrechungen für Remote Benutzer zu vermeiden, wird empfohlen, RDP-Clients bereitzustellen, die die entsprechende Protokollversion unterstützen, bevor Sie die-Eigenschaft aktivieren.

## <a name="syntax"></a>Syntax


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserAuthenticationRequired* \[ in\]
</dt> <dd>

Gibt an, ob eine Benutzerauthentifizierung erforderlich ist.

<dt>

0 (0x0)
</dt> <dd>

Anforderung deaktivieren, dass der Benutzer authentifiziert werden muss

</dd> <dt>

1 (0x1)
</dt> <dd>

Aktiviert die Anforderung, dass der Benutzer authentifiziert werden muss.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

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

[**Win32-Einstellung für "" \_**](win32-tsgeneralsetting.md)
</dt> </dl>

 

