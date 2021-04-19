---
description: Gibt den externen Schlüssel aus einer Datei zurück.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Getexternalkeyfromfile-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355311"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Getexternalkeyfromfile-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getexternalkeyfromfile** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt den externen Schlüssel aus einer Datei zurück, die von [**saveexternalkeytofile**](saveexternalkeytofile-win32-encryptablevolume.md)erstellt wurde, wenn der Speicherort dieser Datei ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pathwithfilename* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Speicherort der Datei angibt, die einen externen Schlüssel enthält.

</dd> <dt>

*ExternalKey* \[ vorgenommen\]
</dt> <dd>

Typ: **Uint8 \[ \]**

Ein Bytearray, bei dem es sich um den in der Datei enthaltenen, externen 256-Bit-Schlüssel handelt, der zum Entsperren eines Volumes verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                   | BESCHREIBUNG                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                  |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Die Datei enthält keinen externen Schlüssel.<br/>  |
| <dl> <dt>**Fehler \_ Die Datei wurde \_ nicht \_ gefunden**</dt> <dt>2147942402 (0x80070002)</dt> . </dl> | Die Datei wurde am angegebenen Speicherort nicht gefunden.<br/> |



 

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

 

 
