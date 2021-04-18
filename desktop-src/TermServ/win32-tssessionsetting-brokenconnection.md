---
title: Brokenconnection-Methode der Win32_TSSessionSetting-Klasse (wtsprodecol. h)
description: Legt die BrokenConnectionAction-Eigenschaft fest. Dies ist die Aktion, die der Server durchführt, wenn das Sitzungszeit Limit erreicht ist, oder, wenn die Verbindung getrennt wird.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Brokenconnection-Methode Remotedesktopdienste
- Brokenconnection-Methode Remotedesktopdienste, Win32_TSSessionSetting-Klasse
- Win32_TSSessionSetting-Klasse Remotedesktopdienste, brokenconnection-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339325"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a>Brokenconnection-Methode der Win32- \_ Klasse "tssessionsetting"

Legt die **BrokenConnectionAction** -Eigenschaft fest. Dies ist die Aktion, die der Server durchführt, wenn das Sitzungszeit Limit erreicht ist, oder, wenn die Verbindung getrennt wird.

## <a name="syntax"></a>Syntax


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BrokenConnectionAction* \[ in\]
</dt> <dd>

Die auszuführende Aktion.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>Verbindung **trennen** (0)


</dt> <dd>

Der Benutzer ist von der Sitzung getrennt.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (1)


</dt> <dd>

Die Sitzung wird dauerhaft vom Server gelöscht.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung unter Gruppenrichtlinie-Steuerelement ist.

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| Header<br/>                   | <dl> <dt>Wtsproum Col. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessionsetting**](win32-tssessionsetting.md)
</dt> </dl>

 

