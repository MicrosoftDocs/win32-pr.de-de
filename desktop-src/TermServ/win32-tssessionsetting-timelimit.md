---
title: TimeLimit-Methode der Win32_TSSessionSetting-Klasse
description: Legt die maximale Zeit fest, die dem angegebenen Sitzungslimittyp zugeordnet ist.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- TimeLimit-Remotedesktopdienste
- TimeLimit-Methode Remotedesktopdienste , Win32_TSSessionSetting-Klasse
- Win32_TSSessionSetting klasse Remotedesktopdienste , TimeLimit-Methode
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
ms.openlocfilehash: 7f49451b1f6b7b2e63079d0bebbcd0dbb43b76352ae3609ce4138b771a01e03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137553"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>TimeLimit-Methode der Win32 \_ TSSessionSetting-Klasse

Legt die maximale Zeit fest, die dem angegebenen Sitzungslimittyp zugeordnet ist.

## <a name="syntax"></a>Syntax


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SessionLimitType* \[ In\]
</dt> <dd>

Gibt den Typ der Sitzungslimiteigenschaft an, die von der -Methode festgelegt wird.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**


</dt> <dd>

Die -Methode setzt die **ActiveSessionLimit-Eigenschaft.**

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**


</dt> <dd>

Die -Methode setzt die **DisconnectedSessionLimit-Eigenschaft.**

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**


</dt> <dd>

Die -Methode setzt die **IdleSessionLimit-Eigenschaft.**

</dd> </dl> </dd> <dt>

*ValueLimit* \[ In\]
</dt> <dd>

Die neue maximale Zeit in Millisekunden für die durch den *SessionLimitType-Parameter angegebene* Eigenschaft. Der Wert 0 (null) gibt an, dass kein Sitzungslimit besteht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Success bei Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> </dl>

 

