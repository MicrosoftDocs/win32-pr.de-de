---
title: Create-Methode der Win32_Terminal-Klasse
description: Erstellt ein Terminal mit Standardeinstellungen, die mithilfe der Eigenschaften und Methoden der Win32 \_ TerminalSetting-Klassen angepasst werden können.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Create-Methode Remotedesktopdienste
- Create Method Remotedesktopdienste, Win32_Terminal-Klasse
- Win32_Terminal Klasse Remotedesktopdienste, Methode erstellen
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475642"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Create-Methode der Win32- \_ Terminal Klasse

Die **Create** -Methode erstellt ein Terminal mit Standardeinstellungen, das mithilfe der Eigenschaften und Methoden der [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) -Klassen angepasst werden kann. Die Funktion gibt bei Erfolg 0 (null) und einen Fehler Fehler zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Newterminalname* \[ in\]
</dt> <dd>

Der Name des Terminals.

</dd> <dt>

*Transport* \[ in\]
</dt> <dd>

Transport für das Terminal. Dies ist eine Eigenschaft der Win32-Klasse " [**\_ tgeneralsetting**](win32-tsgeneralsetting.md) ".

</dd> <dt>

*TerminalProtocol* \[ in\]
</dt> <dd>

Protokoll für das Terminal. Dies ist eine Eigenschaft der Win32-Klasse " [**\_ tgeneralsetting**](win32-tsgeneralsetting.md) ".

</dd> </dl>

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

[**Win32- \_ Terminal**](win32-terminal.md)
</dt> </dl>

 

