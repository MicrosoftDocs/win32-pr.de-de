---
description: Gibt den externen Schlüssel aus einer Datei zurück.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: GetExternalKeyFromFile-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: e2046e64340167a98d838fd5a64324a410b0d0418a740550f9336117e2f1d8d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892428"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>GetExternalKeyFromFile-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetExternalKeyFromFile-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt den externen Schlüssel aus einer Datei zurück, die von [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)erstellt wurde, und gibt dabei den Speicherort dieser Datei zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PathWithFileName* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Speicherort der Datei angibt, die einen externen Schlüssel enthält.

</dd> <dt>

*ExternalKey* \[ out\]
</dt> <dd>

Typ: **uint8 \[ \]**

Ein Bytearray, bei dem es sich um den externen 256-Bit-Schlüssel in der Datei handelt, der zum Entsperren eines Volumes verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.



| Rückgabecode/-wert                                                                                                                                                                   | BESCHREIBUNG                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Die Methode war erfolgreich.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Die Datei enthält keinen externen Schlüssel.<br/>  |
| <dl> <dt>**FEHLER \_ DATEI \_ NICHT \_ GEFUNDEN**</dt> <dt>2147942402 (0x80070002)</dt> </dl> | Die Datei wurde am angegebenen Speicherort nicht gefunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
