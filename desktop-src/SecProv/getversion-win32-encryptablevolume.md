---
description: Gibt die Version der Vollversion des Volumes zurück.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: GetVersion-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354450"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>GetVersion-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **GetVersion** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt die Version der Vollversion des Volumes zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Version* \[ vorgenommen\]
</dt> <dd>

Typ: **UInt32**

Eine Ganzzahl ohne Vorzeichen, die die Metadatenversion des Volumes angibt.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannter**</dt> Wert <dt>0</dt> </dl> | Das Betriebssystem ist unbekannt.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Windows Vista-Format, d. h., das Volume wurde mit BitLocker auf einem Computer mit Windows Vista geschützt.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Windows 7-Format, d. h., das Volume wurde mit BitLocker auf einem Computer mit Windows 7 geschützt, oder das Metadatenformat wurde mit der [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) -Methode aktualisiert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.

Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                               |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>214794287 (0xccd802f)</dt> </dl> | Der Wert für den *Versions* Parameter ist ungültig.<br/> |
| <dl> <dt>**Fehler \_ Ungültige \_ Daten**</dt> <dt>13 (0xD)</dt> </dl>       | Der Treiber hat ein nicht unterstütztes Datenformat zurückgegeben.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
