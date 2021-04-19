---
description: Schreibt den externen Schlüssel, der der angegebenen volumeschlüsselschutzvorrichtung zugeordnet ist, in eine ausgeblendete, schreibgeschützte Datei im angegebenen Ordner.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Saveexternalkeyyfile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349962"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Saveexternalkeyyfile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **saveexternalkeytofile** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " schreibt den externen Schlüssel, der der angegebenen volumeschlüsselschutzvorrichtung zugeordnet ist, in eine ausgeblendete, schreibgeschützte Datei im angegebenen Ordner.

Diese Methode ist nur für Schlüssel Schutzvorrichtungen vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel" anwendbar.

## <a name="syntax"></a>Syntax


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumekeyprotectorid* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichen folgen Bezeichner zum Verwalten einer verschlüsselten volumeschlüsselschutzvorrichtung.

</dd> <dt>

*Pfad* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das Volume oder den Ordner Speicherort enthält, an dem der der angegebenen Schlüssel Schutzvorrichtung zugeordnete externe Schlüssel gespeichert werden soll. Dieser Pfad enthält nicht den Namen der Datei, die intern ist und sich von Version zu Version ändern kann. Verwenden Sie **getexternalkeyfilename** , um den Dateinamen zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                                                                                                             |
| <dl> <dt>**F \_ E \_ gesperrt \_ Volume**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | Das Volume ist gesperrt.<br/>                                                                                                                  |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Der *volumekeyprotectorid-* Parameter verweist nicht auf eine Schlüssel Schutzvorrichtung vom Typ "externer Schlüssel" oder "TPM und Systemstart Schlüssel".<br/>            |
| <dl> <dt>**Fehler \_ Der Pfad wurde \_ nicht \_ gefunden**</dt> <dt>2147942403 (0x80070003)</dt> . </dl> | Der *path* -Parameter verweist nicht auf einen gültigen Speicherort.<br/> Stellen Sie sicher, dass der Dateiname nicht im *path* -Parameter enthalten ist.<br/> |
| <dl> <dt>**F \_ E \_ nicht \_ aktiviert**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüssel Schutzvorrichtung zum Aktivieren von BitLocker hinzu. <br/>                                                      |



 

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

 

 
