---
description: Die isendorsementkeypaunpresent-Methode der Win32- \_ TPM-Klasse gibt an, ob das Endorsement Key-paar auf dem Gerät vorhanden ist.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Isendorsementkeypaarpresent-Methode der Win32_Tpm-Klasse
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
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131988"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Isendorsementkeypaarpresent-Methode der Win32- \_ TPM-Klasse

Die **isendorsementkeypaunpresent** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Endorsement Key-paar auf dem Gerät vorhanden ist. Das Endorsement Key-Paar ist erforderlich, bevor das Gerät im Besitz des Geräts sein kann. Dieses Schlüsselpaar kann mit der Methode " [**kreateendorsegmentkeypair**](createendorsementkeypair-win32-tpm.md) " erstellt werden.

Das Gerät muss aktiviert und aktiviert sein, damit diese Methode erfolgreich ausgeführt werden konnte. Informationen zum Aktivieren und Aktivieren eines nicht eigenen Geräts finden Sie unter der [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode.

## <a name="syntax"></a>Syntax


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isendorsementkeypaarpresent* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

**True** gibt an, dass das Endorsement Key-paar auf dem Gerät vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> <dt>

[**"Kreateendorsegmentkeypair"**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**Setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
