---
title: Die Methode "stenessiondirectoryactive" der Win32_TSSessionDirectory-Klasse
description: Die sezessiondirectoryactive-Methode legt die sessiondirectoryactive-Eigenschaft fest.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "Win32_TSSessionDirectory"
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, Methode "-Klasse"
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391803"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a>Die Methode "c-essiondirectoryactive" der Win32- \_ Klasse "tssessiondirectory"

Die **sezessiondirectoryactive** -Methode legt die **sessiondirectoryactive** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sessiondirectorialactive* \[ in\]
</dt> <dd>

Typ: **UInt32**

Flag zum Deaktivieren oder Aktivieren des Sitzungs Verzeichnis dienstanzen.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Deaktivieren Sie den Sitzungs Verzeichnisdienst.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktivieren Sie den Sitzungs Verzeichnisdienst.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

