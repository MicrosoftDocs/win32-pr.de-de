---
description: Exportiert Informationen, die bei der Wiederherstellung verschlüsselter Daten helfen können, wenn das Laufwerk stark beschädigt ist und keine Datensicherungsdateien vorhanden sind.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: GetKeyPackage-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: 777c68bab142fc0f27d9200d2aea1ff0c45c47181d951600dcc96bb0e623b6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892357"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>GetKeyPackage-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetKeyPackage-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) exportiert Informationen, die bei der Wiederherstellung verschlüsselter Daten helfen können, wenn das Laufwerk stark beschädigt ist und keine Datensicherungsdateien vorhanden sind.

Die exportierten Informationen bestehen aus dem Verschlüsselungsschlüssel des Volumes, der durch eine Schlüsselschutzvorrichtung vom Typ "Numerisches Kennwort" oder "Externer Schlüssel" gesichert wird. Um dieses Paket verwenden zu können, müssen Sie auch das entsprechende numerische Kennwort oder den externen Schlüssel speichern.

> [!IMPORTANT]
> Wenn Sie ein Schlüsselpaket exportieren möchten, stellen Sie sicher, dass diese Informationen an einem gut geschützten Speicherort bleiben. Tragen Sie diese Informationen nicht mit Ihrem Computer. Wenn dieses Schlüsselpaket verloren geht oder gestohlen wird, müssen Sie das Volume entschlüsseln und es mit einem neuen Schlüssel erneut verschlüsseln.

 

Im Falle eines Laufwerkausfalls ist das BitLocker-Reparaturtool vorhanden, um verfügbare Daten zu erhalten. Weitere Informationen dazu, wie dieses Tool das Schlüsselpaket verwenden kann, finden Sie unter How to use [the BitLocker Repair Tool](https://support.microsoft.com/kb/928201)to help recover data from an encrypted volume in Windows Vista .

## <a name="syntax"></a>Syntax


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeKeyProtectorID* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der zum Verwalten einer verschlüsselten Volumeschlüsselschutzvorrichtung verwendet wird. Zum Exportieren eines Schlüsselpakets müssen Sie eine Schlüsselschutzvorrichtung vom Typ "Numerisches Kennwort" oder "Externer Schlüssel" verwenden.

</dd> <dt>

*KeyPackage \[ \]* \[out\]
</dt> <dd>

Typ: **uint8**

Ein Bytestream, der den Verschlüsselungsschlüssel für ein Volume enthält, der durch die angegebene Schlüsselschutzvorrichtung geschützt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Die Methode war erfolgreich.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Das Volume ist gesperrt.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NOT \_ FOUND**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | Die bereitgestellte Schlüsselschutzvorrichtung ist auf dem Volume nicht vorhanden.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ INVALID PROTECTOR TYPE \_ \_ 2150694970**</dt> <dt>(0x8031003A)</dt> </dl> | Der *VolumeKeyProtectorID-Parameter* bezieht sich nicht auf eine Schlüsselschutzvorrichtung vom Typ "Numerisches Kennwort" oder "Externer Schlüssel". Verwenden Sie entweder [**die Methode ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) oder [**ProtectKeyWithExternalKey,**](protectkeywithexternalkey-win32-encryptablevolume.md) um eine Schlüsselschutzvorrichtung des entsprechenden Typs zu erstellen.<br/> |



 

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

 

 
