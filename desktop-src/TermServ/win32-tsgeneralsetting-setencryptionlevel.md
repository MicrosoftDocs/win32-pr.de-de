---
title: SetEncryptionLevel-Methode der Win32_TSGeneralSetting-Klasse
description: Die setencryptionlevel-Methode legt die Verschlüsselungs Stufe fest.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Setencryptionlevel-Methode Remotedesktopdienste
- Setencryptionlevel-Methode Remotedesktopdienste, Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste, setencryptionlevel-Methode
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104595"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Setencryptionlevel-Methode der Win32- \_ Klasse "zgeneralsetting"

Die **setencryptionlevel** -Methode legt die Verschlüsselungs Stufe fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Minverschlüsselungslevel* \[ in\]
</dt> <dd>

Die minimale Verschlüsselungs Stufe, die festgelegt werden soll.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Niedriger Verschlüsselungs Grad. Nur vom Client an den Server gesendete Daten werden mithilfe der 56-Bit-Verschlüsselung verschlüsselt. Beachten Sie, dass die vom Server an den Client gesendeten Daten nicht verschlüsselt sind.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Client kompatibles Verschlüsselungs Niveau Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit der maximalen Schlüssel Stärke verschlüsselt, die vom Client unterstützt wird.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**€**


</dt> <dd>

Hohes Maß an Verschlüsselung. Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit starker 128-Bit-Verschlüsselung verschlüsselt. Clients, die diese Verschlüsselungs Stufe nicht unterstützen, können keine Verbindung herstellen.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Mit der PPS-kompatible Verschlüsselung. Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden verschlüsselt und mit den Federal Information Processing Standard (FI)-Verschlüsselungsalgorithmen mithilfe der Kryptografiemodule von Microsoft entschlüsselt. Der Standardwert für "Sicherheitsanforderungen für kryptografische Module" ist "Standard". In den Informationen zu den in der US-Regierung verwendeten Hardware-und Softwaremodulen werden die behördlichen Anforderungen für Hardware-und Software Kryptografiemodule beschrieben. 2001 140-2 1994 140-1

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

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

 

