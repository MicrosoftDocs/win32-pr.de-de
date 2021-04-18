---
description: Gibt an, ob das Volume bei der Bereitstellung automatisch entsperrt wird.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Isautounlockaktivierte Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340177"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Isautounlockaktivierte Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **isautounlockaktivierte** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob das Volume bei der Bereitstellung automatisch entsperrt wird (z. b. Wenn Wechselmedien mit dem Computer verbunden sind).

## <a name="syntax"></a>Syntax


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isautounlockaktivierte* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

Ein boolescher Wert, der true ist, wenn der zum automatischen Entsperren des Volumes verwendete externe Schlüssel vorhanden ist und auf dem momentan laufenden Betriebssystem Volume gespeichert ist, andernfalls false.

</dd> <dt>

*Volumekeyprotectorid* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner, der die zugeordnete verschlüsselte volumeschlüsselschutzkennung enthält, wenn *isautounlockaktiviaktiviert* ist.

Wenn *isautounlockaktivierte* den Wert false hat, ist *volumekeyprotectorid* eine leere Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                     | BESCHREIBUNG                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | Die Methode war erfolgreich.<br/>                                                       |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu.<br/> |
| <dl> <dt>**F \_ E \_ Not \_ Data \_ Volume**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | Die Methode kann nicht für das aktuell laufende Betriebssystem Volume ausgeführt werden.<br/>      |



 

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

 

 
