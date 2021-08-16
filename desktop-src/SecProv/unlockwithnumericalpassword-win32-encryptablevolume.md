---
description: Verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumens.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: UnlockWithNumericalPassword-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d52cd0dd2c80bf00a55bef0fde40008f7133f28cb3be0a9aa5366076c6502b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891294"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>UnlockWithNumericalPassword-Methode der Win32 \_ EncryptableVolume-Klasse

Die **UnlockWithNumericalPassword-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) verwendet ein bereitgestelltes numerisches Kennwort für den Zugriff auf den Inhalt eines Datenvolumes.

Der Verschlüsselungsschlüssel des Volumes muss mit einer oder mehrere Schlüsselschutzvorrichtungen des Typs "Numerisches Kennwort" (mithilfe der [**ProtectKeyWithNumericalPassword-Methode)**](protectkeywithnumericalpassword-win32-encryptablevolume.md) gesichert worden sein, um das Volume mit dieser Methode entsperren zu können.

> [!Note]  
> Wenn der Datenträger Hardwareverschlüsselung unterstützt, legt diese Funktion den Bandstatus auf "Entsperrt" fest.

 

## <a name="syntax"></a>Syntax


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumericalPassword* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das numerische Kennwort angibt.

Das numerische Kennwort muss 48 Ziffern enthalten. Diese Ziffern können in acht Gruppen von sechs Ziffern unterteilt werden, und die letzte Ziffer in jeder Gruppe gibt einen Prüfsummenwert für die Gruppe an. Jede Gruppe von 6 Ziffern muss durch 11 teilbar sein und kleiner als 65536 sein. Wenn eine Gruppe von sechs Ziffern als x1, x2, x3, x4, x5 und x6 bezeichnet wird, wird die Prüfsumme x6-Ziffer als –x1+x2–x3+x4-x5 mod 11 berechnet.

Die Gruppen von Ziffern können optional durch ein Leerzeichen oder bindestrich getrennt werden. Daher können "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" ebenfalls gültige numerische Kennwörter enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn das Volume bereits entsperrt ist und keine anderen Fehler auftreten, gibt diese Methode 0 zurück.



| Rückgabecode/-wert                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | Die Methode war erfolgreich.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NOT \_ FOUND**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | Das Volume verfügt nicht über eine Schlüsselschutzvorrichtung vom Typ "Numerisches Kennwort".<br/> Der *Parameter NumericalPassword* hat ein gültiges Format, Sie können jedoch kein numerisches Kennwort verwenden, um das Volume zu entsperren.<br/>           |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | Der *Parameter NumericalPassword* kann das Volume nicht entsperren.<br/> Eine oder mehrere Schlüsselschutzvorrichtungen vom Typ "Numerisches Kennwort" sind vorhanden, aber der angegebene *NumericalPassword-Parameter* kann das Volume nicht entsperren.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ UNGÜLTIGES \_ KENNWORTFORMAT**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | Der *Parameter NumericalPassword* hat kein gültiges Format.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
