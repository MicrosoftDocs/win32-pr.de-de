---
description: Erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Discovery-Volumes.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Preparevolume-Methode der Win32_EncryptableVolume-Klasse
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
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128749"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Preparevolume-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **preparevolume** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " erstellt ein BitLocker-Volume mit dem angegebenen Dateisystemtyp des Discovery-Volumes. Diese Methode muss aufgerufen werden, bevor das Volume mit einer der **protectkeywith \** _-Methoden geschützt werden kann.

## <a name="syntax"></a>Syntax

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

_DiscoveryVolumeType * \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die den Typ des Ermittlungs Volumens angibt.

| Wert               | Bedeutung                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;gar&gt;**    | Kein suchvolume. Dieser Wert erstellt ein System eigenes BitLocker-Volume. |
| **&lt;vorgegebene&gt;** | Dieser Wert ist das Standardverhalten.                                |
| **FAT32**           | Dieser Wert erstellt ein FAT32-Ermittlungs Volume.                       |

</dd> <dt>

*Forceverschlüsseltiontype* \[ in\]
</dt> <dd>

Typ: **UInt32**

Eine ganze Zahl, die den Verschlüsselungstyp angibt. Dies kann einer der folgenden Werte sein:

| Wert                                                                                                                                                                                                                                       | Bedeutung                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Nicht angegeben**</dt> <dt>0</dt> </dl> | Der Verschlüsselungstyp ist nicht angegeben.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Software Verschlüsselung.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Hardware Verschlüsselung.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

| Rückgabecode/-wert      | BESCHREIBUNG                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | Die Methode war erfolgreich.<br/> |

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Methode beim Aktivieren eines BitLocker-Volumes nicht aufrufen, entspricht dies dem Aufrufen dieser Methode mit dem Standardwert im *discoveryvolumetype* -Parameter.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
