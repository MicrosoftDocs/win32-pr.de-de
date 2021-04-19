---
title: Setmaxconnections-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt die Eigenschaften MaxConnections und UnlimitedConnections fest, die die maximale Anzahl zulässiger Verbindungen mit dem Remotedesktop Gateway-Server (RD-Gateway) steuern.
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Setmaxconnections-Methode Remotedesktopdienste
- Setmaxconnections-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setmaxconnections-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341401"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a>Setmaxconnections-Methode der Win32-Klasse "t- \_ gatewayserversettings"

Legt die Eigenschaften **MaxConnections** und **UnlimitedConnections** fest, die die maximale Anzahl zulässiger Verbindungen mit dem Remotedesktop Gateway-Server (RD-Gateway) steuern.

## <a name="syntax"></a>Syntax


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindungen* \[ in\]
</dt> <dd>

Anzahl von Verbindungen, die von diesem Server akzeptiert werden sollen. Legen Sie für eine unbegrenzte Anzahl von Verbindungen den *isunlimited* -Parameter auf " **true**" fest.

</dd> <dt>

*Isunbegrenzt* \[ in\]
</dt> <dd>

**True** gibt an, dass Verbindungen mit dem Dienst nicht auf eine bestimmte Anzahl beschränkt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

