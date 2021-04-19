---
description: Ruft das numerische Kennwort für eine angegebene Schlüssel Schutzvorrichtung ab.
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
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346293"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a>GetKeyProtectorNumericalPassword-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **GetKeyProtectorNumericalPassword** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft das numerische Kennwort für eine bestimmte Schlüssel Schutzvorrichtung des entsprechenden Typs ab.

Die schlüsselschutzschutzkennung muss auf eine Schlüssel Schutzvorrichtung vom Typ "numerisches Kennwort" verweisen.

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> <dt>

*Numericalpassword* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das Kennwort darstellt, das zum Entsperren des entsprechenden Volumes verwendet werden kann.

Das numerische Kennwort ist 48 Ziffern. Diese Ziffern sind in acht Gruppen von 6 Ziffern unterteilt, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt. Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 gekennzeichnet ist, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.

Die Gruppen von Ziffern sind durch einen Bindestrich getrennt. Daher ist "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" das Format des zurückgegebenen Kennworts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                               |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>                                                                                    |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort".<br/> |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
