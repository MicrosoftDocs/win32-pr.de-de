---
title: Connectionsettings-Methode der Win32_TSClientSetting-Klasse
description: Die connectionsettings-Methode legt die Sitzungs Einstellungen fest, die für die Verbindung und den Anmeldeprozess gelten.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Connectionsettings-Methode Remotedesktopdienste
- Connectionsettings-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, connectionsettings-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517675"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Connectionsettings-Methode der Win32- \_ Klasse "tsclientsetting"

Die **connectionsettings** -Methode legt die Sitzungs Einstellungen fest, die für die Verbindung und den Anmeldeprozess gelten.

## <a name="syntax"></a>Syntax


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Connectclientdrivesatlogon* \[ in\]
</dt> <dd>

Flag zum Aktivieren oder Deaktivieren der **connectclientdrivesatlogon** -Eigenschaft, die angibt, ob die Laufwerke des Clients während des Anmeldevorgangs automatisch verbunden werden.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Die Laufwerke des Clients werden nicht automatisch verbunden.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Die Laufwerke des Clients werden automatisch verbunden.

</dd> </dl> </dd> <dt>

*Connectprinteratlogon* \[ in\]
</dt> <dd>

Flag zum Aktivieren oder Deaktivieren der **connectprinteratlogon** -Eigenschaft, die angibt, ob alle zugeordneten lokalen Client Drucker während des Anmeldevorgangs automatisch verbunden werden.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Alle zugeordneten lokalen Drucker sind nicht automatisch verbunden.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Alle zugeordneten lokalen Drucker werden automatisch verbunden.

</dd> </dl> </dd> <dt>

*Defaultdeclientprinter* \[ in\]
</dt> <dd>

Flag zum Aktivieren oder Deaktivieren der **defaultdeclientprinter** -Eigenschaft, die angibt, ob Druckaufträge automatisch an den lokalen Drucker des Clients gesendet werden.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Druckaufträge werden nicht automatisch gesendet.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Druckaufträge werden automatisch gesendet.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.

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

[**Win32- \_ tsclientsetting**](win32-tsclientsetting.md)
</dt> </dl>

 

