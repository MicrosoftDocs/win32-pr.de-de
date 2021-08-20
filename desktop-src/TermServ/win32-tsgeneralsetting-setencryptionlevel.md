---
title: SetEncryptionLevel-Methode der Win32_TSGeneralSetting-Klasse
description: Die SetEncryptionLevel-Methode legt die Verschlüsselungsebene fest.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- SetEncryptionLevel-Methode Remotedesktopdienste
- SetEncryptionLevel-Methode Remotedesktopdienste , Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting Klasse Remotedesktopdienste , SetEncryptionLevel-Methode
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
ms.openlocfilehash: a54aacf931a66d6d4bdd4daa24a6432e4caa7fb01695aebbe4324b17ab5f2bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348842"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>SetEncryptionLevel-Methode der Win32 \_ TSGeneralSetting-Klasse

Die **SetEncryptionLevel-Methode** legt die Verschlüsselungsebene fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MinEncryptionLevel* \[ In\]
</dt> <dd>

Die festzulegende Mindestverschlüsselungsebene.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Niedrige Verschlüsselungsebene. Nur daten, die vom Client an den Server gesendet werden, werden mit 56-Bit-Verschlüsselung verschlüsselt. Beachten Sie, dass die vom Server an den Client gesendeten Daten nicht verschlüsselt sind.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Clientkompatible Verschlüsselungsebene. Alle Daten, die von Client zu Server und von Server zu Client gesendet werden, werden mit der maximalen Schlüsselstärke verschlüsselt, die vom Client unterstützt wird.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Hoher Verschlüsselungsgrad. Alle Daten, die von Client zu Server und von Server zu Client gesendet werden, werden mit starker 128-Bit-Verschlüsselung verschlüsselt. Clients, die diese Verschlüsselungsebene nicht unterstützen, können keine Verbindung herstellen.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

FIPS-kompatible Verschlüsselung. Alle Daten, die von Client zu Server und von Server zu Client gesendet werden, werden mit den FIPS-Verschlüsselungsalgorithmen (Federal Information Processing Standard) mithilfe der kryptografischen Microsoft-Module verschlüsselt und entschlüsselt. FIPS ist ein Standard mit dem Titel "Sicherheitsanforderungen für kryptografische Module". FIPS 140-1 (1994) und FIPS 140-2 (2001) beschreiben die Anforderungen der Regierung für Hardware- und Software-Kryptografiemodule, die innerhalb der US-Regierung verwendet werden.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> </dl>

 

