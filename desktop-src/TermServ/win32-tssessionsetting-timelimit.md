---
title: Timelimit-Methode der Win32_TSSessionSetting-Klasse
description: Legt die maximale Zeit fest, die dem angegebenen Sitzungs Beschränkungstyp zugeordnet ist.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Timelimit-Methode Remotedesktopdienste
- Timelimit-Methode Remotedesktopdienste, Win32_TSSessionSetting-Klasse
- Win32_TSSessionSetting-Klasse Remotedesktopdienste, timelimit-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517396"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>Timelimit-Methode der Win32- \_ Klasse "tssessionsetting"

Legt die maximale Zeit fest, die dem angegebenen Sitzungs Beschränkungstyp zugeordnet ist.

## <a name="syntax"></a>Syntax


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SessionLimitType* \[ in\]
</dt> <dd>

Gibt den Typ der Sitzungs Limit-Eigenschaft an, die von der-Methode festgelegt wird.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**


</dt> <dd>

Die-Methode legt die **ActiveSessionLimit** -Eigenschaft fest.

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**


</dt> <dd>

Die-Methode legt die **DisconnectedSessionLimit** -Eigenschaft fest.

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**


</dt> <dd>

Die-Methode legt die **IdleSessionLimit** -Eigenschaft fest.

</dd> </dl> </dd> <dt>

*ValueLimit* \[ in\]
</dt> <dd>

Die neue maximale Zeit (in Millisekunden) für die Eigenschaft, die vom *SessionLimitType* -Parameter angegeben wird. Der Wert 0 (null) gibt an, dass keine Sitzungs Beschränkung vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

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

[**Win32- \_ tssessionsetting**](win32-tssessionsetting.md)
</dt> </dl>

 

