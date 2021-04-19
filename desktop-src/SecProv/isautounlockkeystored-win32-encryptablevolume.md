---
description: Gibt an, ob externe Schlüssel oder zugehörige Informationen, die möglicherweise zum automatischen Entsperren von Datenvolumes verwendet werden, auf dem aktuell laufenden Betriebssystem Volume vorhanden sind.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Isautounlockkeygespeich-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369738"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Isautounlockkeygespeicherte-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **isautounlockkeygespeich-** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob externe Schlüssel oder verwandte Informationen, die möglicherweise zum automatischen Entsperren von Datenvolumes verwendet werden, im aktuell ausgelaufenden Betriebssystem Volume vorhanden sind.

## <a name="syntax"></a>Syntax


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isautounlockkeygespeicherter* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

Ist **true** , wenn alle Informationen, die zum automatischen Entsperren von Datenvolumes verwendet werden können, in der Registrierung des aktuell laufenden Betriebssystem Volume gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                   | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/> |
| <dl> <dt>**F \_ E \_ Not \_ OS \_ Volume**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Die-Methode kann nur für das aktuell laufende Betriebssystem Volume ausgeführt werden.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**clearallautounlockkeys**](clearallautounlockkeys-win32-encryptablevolume.md) , um alle entsperrenden Informationen aus dem momentan ausgelaufenden Betriebssystem Volume zu entfernen.

Die zum Entsperren eines Volumes verwendeten Informationen werden gespeichert, wenn [**enableautounlock**](enableautounlock-win32-encryptablevolume.md) für ein Daten Volume ausgeführt wird, während das aktuell laufende Betriebssystem Volume ausgeführt wird.

" **Isautounlockkey}** " unterscheidet sich von " [**isautounlockkey}**](isautounlockenabled-win32-encryptablevolume.md) " in "", dass auch dann, wenn die automatische Entsperrung für alle Daten Volumes deaktiviert ist, die mit dem Computer verbunden sind, möglicherweise weiterhin Informationen zu nicht mehr vorhandenen Datenvolumen oder Datenvolumes verfügbar sind.

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

 

 
