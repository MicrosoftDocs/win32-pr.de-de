---
description: Sichert den Verschlüsselungsschlüssel des Volumes mit einem externen 256-Bit-Schlüssel.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: ProtectKeyWithExternalKey-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 63ef4f998d576ecf2931af529a0ff6710a54513cc0d19027421c160bbdcd4cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004418"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a>ProtectKeyWithExternalKey-Methode der Win32 \_ EncryptableVolume-Klasse

Die **ProtectKeyWithExternalKey-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) schützt den Verschlüsselungsschlüssel des Volumes mit einem externen 256-Bit-Schlüssel. Dieser externe Schlüssel kann verwendet werden, um nach Authentifizierungsfehlern anderer Schlüsselschutzvorrichtungen (z. B. TPM) wiederherzustellen.

Verwenden Sie die [**SaveExternalKeyToFile-Methode,**](saveexternalkeytofile-win32-encryptablevolume.md) um diesen externen Schlüssel in einer Datei zu speichern. USB-Speichergeräte, die diesen externen Schlüssel enthalten, können beim Starten des Computers als Startschlüssel oder Wiederherstellungsschlüssel verwendet werden.

Für das Volume wird eine Schlüsselschutzvorrichtung vom Typ "Externer Schlüssel" erstellt.

## <a name="syntax"></a>Syntax


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FriendlyName* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die einen vom Benutzer zugewiesenen Bezeichner für diese Schlüsselschutzvorrichtung angibt. Wenn dieser Parameter nicht angegeben ist, wird ein leerer Wert verwendet.

</dd> <dt>

*ExternalKey* \[ in, optional\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, das den externen 256-Bit-Schlüssel angibt, der zum Entsperren des Volumes verwendet wird.

Wenn kein externer Schlüssel angegeben wird, wird nach dem Zufallsprinzip ein Schlüssel generiert. Verwenden Sie die [**GetKeyProtectorExternalKey-Methode,**](getkeyprotectorexternalkey-win32-encryptablevolume.md) um den zufällig generierten Schlüssel abzurufen.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird.

Wenn das Laufwerk Hardwareverschlüsselung unterstützt und BitLocker keinen Bandbesitz übernommen hat, wird die ID-Zeichenfolge auf "BitLocker" festgelegt, und die Schlüsselschutzvorrichtung wird pro Bandmetadaten in geschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Der *ExternalKey-Parameter* wird bereitgestellt, ist aber kein Array der Größe 4.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Das Volume ist gesperrt.<br/>                                                             |
| <dl> <dt>**FVE \_ E \_ NICHT \_ AKTIVIERT**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/> |



 

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

 

 
