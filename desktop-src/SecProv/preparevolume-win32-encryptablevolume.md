---
description: Erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Ermittlungsvolumens.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: PrepareVolume-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 67b36703883825d4144037c54ffb55c00308ed1cfb8ee3e4b074d75d63bf7390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891546"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>PrepareVolume-Methode der Win32 \_ EncryptableVolume-Klasse

Die **PrepareVolume-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Ermittlungsvolumes. Diese Methode muss aufgerufen werden, bevor das Volume mit einer der **ProtectKeyWith-Methoden \* geschützt werden** kann.

## <a name="syntax"></a>Syntax

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*DiscoveryVolumeType* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Typ des Ermittlungsvolumens angibt.

| Wert               | Bedeutung                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;nichts&gt;**    | Kein Ermittlungsvolumen. Dieser Wert erstellt ein natives BitLocker-Volume. |
| **&lt;Standard&gt;** | Dieser Wert ist das Standardverhalten.                                |
| **FAT32**           | Dieser Wert erstellt ein FAT32-Ermittlungsvolumen.                       |

</dd> <dt>

*ForceEncryptionType* \[ In\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl, die den Verschlüsselungstyp angibt. Dies kann einer der folgenden Werte sein.

| Wert                                                                                                                                                                                                                                       | Bedeutung                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Nicht angegeben 0**</dt> <dt></dt> </dl> | Der Verschlüsselungstyp ist nicht angegeben.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Softwareverschlüsselung.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Hardwareverschlüsselung.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

| Rückgabecode/-wert      | BESCHREIBUNG                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | Die Methode war erfolgreich.<br/> |

## <a name="remarks"></a>Hinweise

Wenn Sie diese Methode beim Aktivieren eines BitLocker-Volumes nicht aufrufen, ist dies dasselbe wie das Aufrufen dieser Methode mit dem Standardwert im *DiscoveryVolumeType-Parameter.*

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
