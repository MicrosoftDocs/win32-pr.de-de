---
description: Die IsEndorsementKeyPairPresent-Methode der Win32 \_ Tpm-Klasse gibt an, ob das Endorsement Key-Paar auf dem Gerät vorhanden ist.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: IsEndorsementKeyPairPresent-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: bcbc0c4877aae2db0e94d42838100720ee0ae0dcbdcc33f52cf70d2e23327e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004468"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>IsEndorsementKeyPairPresent-Methode der Win32 \_ Tpm-Klasse

Die **IsEndorsementKeyPairPresent-Methode** der [**Win32 \_ Tpm-Klasse**](win32-tpm.md) gibt an, ob das Endorsement Key-Paar auf dem Gerät vorhanden ist. Das Endorsement Key-Paar ist erforderlich, bevor sich das Gerät im Besitz des Geräts befinden kann. Dieses Schlüsselpaar kann mit der [**CreateEndorsementKeyPair-Methode**](createendorsementkeypair-win32-tpm.md) erstellt werden.

Das Gerät muss aktiviert und aktiviert sein, damit diese Methode erfolgreich ausgeführt werden kann. Informationen zum Aktivieren und Aktivieren eines nicht verwendeten Geräts finden Sie in der [**SetPhysicalPresenceRequest-Methode.**](setphysicalpresencerequest-win32-tpm.md)

## <a name="syntax"></a>Syntax


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

True gibt an, dass das Endorsement Key-Paar auf dem Gerät vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Alle TPM-Fehler sowie Fehler, die spezifisch für TPM-Basisdienste sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
