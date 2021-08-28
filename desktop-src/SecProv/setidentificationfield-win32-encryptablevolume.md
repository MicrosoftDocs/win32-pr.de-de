---
description: Legt die angegebene Bezeichnerzeichenfolge in den Metadaten des Volumes fest.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: SetIdentificationField-Methode der Win32_EncryptableVolume Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 473b10bda95177fa2019a7439b46b475ac3bb8477ef45e19d945e8a7c1bc87a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004268"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a>SetIdentificationField-Methode der Win32 \_ EncryptableVolume-Klasse

Die **SetIdentificationField-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) legt die angegebene Bezeichnerzeichenfolge in den Metadaten des Volumes fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IdentificationField* \[ in, optional\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das Identifikationsfeld angibt, das dem Volume zugewiesen ist. Wenn die optionale Zeichenfolge nicht vorhanden ist, werden die Registrierungssatzwerte verwendet. Wenn die Zeichenfolge vorhanden und nicht leer ist, wird der angegebene Wert verwendet. Beim *IdentificationField-Parameter* wird die Kleinschreibung nicht beachtet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                                  | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Die Methode war erfolgreich.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Dieses Laufwerk wird durch einen BitLocker-Laufwerkverschlüsselung. Sie müssen dieses Volume aus der Systemsteuerung. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker ist auf dem Volume nicht aktiviert. Fügen Sie eine Schlüsselschutzvorrichtung hinzu, um BitLocker zu aktivieren. <br/>                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




