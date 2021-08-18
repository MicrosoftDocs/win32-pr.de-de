---
description: Ruft das numerische Kennwort für eine bestimmte Schlüsselschutzvorrichtung ab.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: GetKeyProtectorNumericalPassword-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a97740338b55238a441c2f08dedf4324144625e3bc58a684f36f0ae98886e0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100640"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorNumericalPassword-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyProtectorNumericalPassword-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) ruft das numerische Kennwort für eine bestimmte Schlüsselschutzvorrichtung des entsprechenden Typs ab.

Der Schlüsselschutzvorrichtungsbezeichner muss auf eine Schlüsselschutzvorrichtung vom Typ "Numerisches Kennwort" verweisen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*NumericalPassword* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das Kennwort darstellt, das zum Entsperren des entsprechenden Volumes verwendet werden kann.

Das numerische Kennwort ist 48 Ziffern. Diese Ziffern werden in acht Gruppen von 6 Ziffern unterteilt, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummenwert für die Gruppe angibt. Wenn eine Gruppe von sechs Ziffern als x1, x2, x3, x4, x5 und x6 bezeichnet wird, wird die x6-Prüfsummenziffer als –x1+x2–x3+x4–x5 mod 11 berechnet.

Die Zifferngruppen werden durch einen Bindestrich getrennt. Daher ist "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" das Format des zurückgegebenen Kennworts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                  | Beschreibung                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                               |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *Parameter VolumeKeyProtectorID* verweist nicht auf eine Schlüsselschutzvorrichtung vom Typ "Numerisches Kennwort".<br/> |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                        |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
