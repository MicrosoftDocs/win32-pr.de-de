---
title: Islogeventaktivierte Methode der Win32_TSGatewayServerSettings-Klasse
description: Gibt an, ob der angegebene Ereignis protokolllistyp aktiviert ist.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Islogeventaktivierte Methode Remotedesktopdienste
- Islogeventaktivierte Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste, islogeventaktivierte Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345306"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Islogeventaktivierte Methode der Win32-Klasse "t- \_ gatewayserversettings"

Gibt an, ob der angegebene Ereignis protokolllistyp aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EventName* \[ in\]
</dt> <dd>

Der Name des Ereignisprotokoll Typs. Dieser Wert sollte mithilfe der [**getlogeventname**](getlogeventname-win32-tsgatewayserversettings.md) -Methode abgerufen werden.

<dt>

Logchanneldisconnect
</dt> <dd>

Der Benutzer hat die Verbindungen mit der Ressource erfolgreich getrennt.

</dd> <dt>

Logfailedchannelconnect
</dt> <dd>

Der Benutzer konnte keine Verbindung mit der Ressource herstellen.

</dd> <dt>

Logfailurumetworkaccesscheck
</dt> <dd>

Fehler bei der Verbindungs Autorisierung des Benutzers

</dd> <dt>

Logfailureresourceaccesscheck
</dt> <dd>

Fehler beim Autorisieren der Ressource.

</dd> <dt>

Logerfolgreicher schannelconnect
</dt> <dd>

Der Benutzer hat erfolgreich eine Verbindung mit der Ressource hergestellt.

</dd> <dt>

Logsuccess-networkaccesscheck
</dt> <dd>

Der Benutzer hat die Verbindungs Autorisierung erfolgreich abgeschlossen.

</dd> <dt>

Logsuccess fulresourceaccesscheck
</dt> <dd>

Der Benutzer hat die Ressourcen Autorisierung erfolgreich abgeschlossen.

</dd> </dl> </dd> <dt>

*Aktiviert* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob der angegebene Ereignis protokolllistyp aktiviert ist.

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
</dt> <dt>

[**Getlogeventname**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

