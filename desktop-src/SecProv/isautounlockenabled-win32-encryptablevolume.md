---
description: Gibt an, ob das Volume automatisch entsperrt wird, wenn es bereitgestellt wird.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: IsAutoUnlockEnabled-Methode der Win32_EncryptableVolume Klasse
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
ms.openlocfilehash: 19437bf40d27bea87103beecfbe8bee71e404c054ace46cb9728f7ac992b5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891911"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>IsAutoUnlockEnabled-Methode der Win32 \_ EncryptableVolume-Klasse

Die **IsAutoUnlockEnabled-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt an, ob das Volume automatisch entsperrt wird, wenn es bereitgestellt wird (z. B. wenn Wechseldatenträger mit dem Computer verbunden sind).

## <a name="syntax"></a>Syntax


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsAutoUnlockEnabled* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

Ein boolescher Wert, der true ist, wenn der externe Schlüssel, der zum automatischen Entsperren des Volumes verwendet wird, vorhanden ist und auf dem aktuell ausgeführten Betriebssystem-Volume gespeichert wurde, andernfalls false.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Ein eindeutiger Zeichenfolgenbezeichner, der die zugeordnete verschlüsselte Volumeschlüsselschutz-ID enthält, wenn *IsAutoUnlockEnabled* true ist.

Wenn *IsAutoUnlockEnabled* false ist, *ist VolumeKeyProtectorID* eine leere Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                     | BESCHREIBUNG                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | Die Methode war erfolgreich.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | Die -Methode kann nicht für das derzeit ausgeführte Betriebssystem-Volume ausgeführt werden.<br/>      |



 

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

 

 
