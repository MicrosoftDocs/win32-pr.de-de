---
title: ConnectionSettings-Methode der Win32_TSClientSetting-Klasse
description: Die ConnectionSettings-Methode legt die Sitzungseinstellungen fest, die für den Verbindungs- und Anmeldevorgang gelten.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- ConnectionSettings-Methode Remotedesktopdienste
- ConnectionSettings-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , ConnectionSettings-Methode
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
ms.openlocfilehash: e3f48a93959b1e86eb77f6ab0fbfab444444ca1c077835e1c28330d34ed66c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656170"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>ConnectionSettings-Methode der Win32 \_ TSClientSetting-Klasse

Die **ConnectionSettings-Methode** legt die Sitzungseinstellungen fest, die für den Verbindungs- und Anmeldevorgang gelten.

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

*ConnectClientDrivesAtLogon* \[ In\]
</dt> <dd>

Flag zum Aktivieren oder Deaktivieren der **ConnectClientDrivesAtLogon-Eigenschaft,** die angibt, ob die Laufwerke des Clients während der Anmeldung automatisch verbunden werden.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Die Laufwerke des Clients werden nicht automatisch verbunden.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Die Laufwerke des Clients werden automatisch verbunden.

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[ In\]
</dt> <dd>

Flag zum Aktivieren oder Deaktivieren der **ConnectPrinterAtLogon-Eigenschaft,** die angibt, ob alle zugeordneten lokalen Clientdrucker während der Anmeldung automatisch verbunden werden.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Alle zugeordneten lokalen Drucker werden nicht automatisch verbunden.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Alle zugeordneten lokalen Drucker werden automatisch verbunden.

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[ In\]
</dt> <dd>

Flag zum Aktivieren oder Deaktivieren der **DefaultToClientPrinter-Eigenschaft,** die angibt, ob Druckaufträge automatisch an den lokalen Drucker des Clients gesendet werden.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Druckaufträge werden nicht automatisch gesendet.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Druckaufträge werden automatisch gesendet.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

