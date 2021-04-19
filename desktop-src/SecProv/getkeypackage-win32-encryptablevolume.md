---
description: Exportiert Informationen, die möglicherweise zum retten verschlüsselter Daten beitragen, wenn das Laufwerk stark beschädigt ist und keine Daten Sicherungsdateien vorhanden sind.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Getkeypackage-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359439"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Getkeypackage-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getkeypackage** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " exportiert Informationen, die möglicherweise dazu beitragen, verschlüsselte Daten zu retten, wenn das Laufwerk stark beschädigt ist und keine Daten Sicherungsdateien vorhanden sind.

Die exportierten Informationen bestehen aus dem Verschlüsselungsschlüssel des Volumes, der durch eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel" gesichert ist. Um dieses Paket verwenden zu können, müssen Sie auch das entsprechende numerische Kennwort oder den externen Schlüssel speichern.

> [!IMPORTANT]
> Wenn Sie sich für das Exportieren eines Schlüssel Pakets entscheiden, stellen Sie sicher, dass diese Informationen an einem gut geschützten Speicherort aufbewahrt werden. Diese Informationen dürfen nicht auf Ihrem Computer enthalten sein. Wenn das Schlüssel Paket verloren geht oder gestohlen wird, müssen Sie das Volume entschlüsseln und mit einem neuen Schlüssel erneut verschlüsseln.

 

Im Fall eines Laufwerks Fehlers ist das BitLocker-Reparatur Tool vorhanden, um die verfügbaren Daten zu retten. Weitere Informationen zur Verwendung des Schlüssel Pakets durch dieses Tool finden [Sie unter Verwenden des BitLocker-Reparatur Tools zum Wiederherstellen von Daten von einem verschlüsselten Volume in Windows Vista](https://support.microsoft.com/kb/928201).

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung. Zum Exportieren eines Schlüssel Pakets müssen Sie eine Schlüssel Schutzvorrichtung vom Typ "numerisch Password" oder "externer Schlüssel" verwenden.

</dd> <dt>

*KeyPackage \[ \]* \[out\]
</dt> <dd>

Typ: **Uint8**

Ein Bytestream, der den Verschlüsselungsschlüssel für ein Volume enthält, gesichert durch die angegebene Schlüssel Schutzvorrichtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**F \_ E \_ Protector \_ nicht \_ gefunden**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Die angegebene Schlüssel Schutzvorrichtung ist auf dem Volume nicht vorhanden.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**F \_ E \_ ungültiger \_ \_ schutzschutztyp**</dt> <dt>2150694970 (0x8031003a)</dt> </dl> | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung des Typs "numerisches Kennwort" oder "externer Schlüssel". Verwenden Sie entweder die [**protectkeywithnumericalpassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) -Methode oder die [**protectkeywithexternalkey**](protectkeywithexternalkey-win32-encryptablevolume.md) -Methode, um eine Schlüssel Schutzvorrichtung des entsprechenden Typs zu erstellen.<br/> |



 

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

 

 
