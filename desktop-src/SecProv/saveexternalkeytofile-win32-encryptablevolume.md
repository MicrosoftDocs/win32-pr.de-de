---
description: Schreibt den externen Schlüssel, der der angegebenen Volumeschlüsselschutzvorrichtung zugeordnet ist, in eine ausgeblendete, schreibgeschützte Datei im angegebenen Ordner.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: SaveExternalKeyToFile-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 02269d2b2339ebc8a2b6022bc5f02e63710d496e768be09dad9993c177ed5de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004288"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>SaveExternalKeyToFile-Methode der Win32 \_ EncryptableVolume-Klasse

Die **SaveExternalKeyToFile-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) schreibt den externen Schlüssel, der der angegebenen Volumeschlüsselschutzvorrichtung zugeordnet ist, in eine ausgeblendete, schreibgeschützte Systemdatei im angegebenen Ordner.

Diese Methode gilt nur für Schlüsselschutzvorrichtungen vom Typ "Externer Schlüssel" oder "TPM und Startschlüssel".

## <a name="syntax"></a>Syntax


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

</dd> <dt>

*Pfad* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das Volume oder den Ordnerspeicherort enthält, an dem der der angegebenen Schlüsselschutzvorrichtung zugeordnete externe Schlüssel gespeichert werden soll. Dieser Pfad enthält nicht den Namen der Datei, der intern ist und von Version zu Version geändert werden kann. Verwenden **Sie GetExternalKeyFileName,** um den Dateinamen zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                   | Beschreibung                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | Das Volume ist gesperrt.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Der *Parameter VolumeKeyProtectorID* bezieht sich nicht auf eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel" oder "TPM und Startschlüssel".<br/>            |
| <dl> <dt>**FEHLER \_ PATH \_ NOT \_ FOUND**</dt> <dt>2147942403 (0x80070003)</dt> </dl> | Der *Path-Parameter* bezieht sich nicht auf einen gültigen Speicherort.<br/> Stellen Sie sicher, dass der Dateiname nicht im *Path-Parameter enthalten* ist.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                      |



 

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

 

 
