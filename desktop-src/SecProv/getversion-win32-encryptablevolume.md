---
description: Gibt die FVE-Metadatenversion des Volumes zurück.
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
ms.openlocfilehash: 0681498a0d075fa22bada520e22c0ae626a4764d1a917f7090b796f05d66b122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891901"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>GetVersion-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetVersion-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) gibt die FVE-Metadatenversion des Volumes zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Version* \[ out\]
</dt> <dd>

Typ: **uint32**

Eine ganze Zahl ohne Vorzeichen, die die Metadatenversion des Volumes angibt.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl> | Das Betriebssystem ist unbekannt.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Windows Vista-Format, d. h. das Volume wurde mit BitLocker auf einem Computer geschützt, auf dem Windows Vista ausgeführt wird.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Windows 7 Format, d. h. das Volume wurde mit BitLocker auf einem Computer mit Windows 7 geschützt, oder das Metadatenformat wurde mithilfe der [**UpgradeVolume-Methode**](upgradevolume-win32-encryptablevolume.md) aktualisiert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn er fehlschlägt.

Wenn das Volume bereits entsperrt ist und keine weiteren Fehler auftreten, gibt diese Methode 0 (null) zurück.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | Der Wert für den *Version-Parameter* ist ungültig.<br/> |
| <dl> <dt>**FEHLER \_ INVALID \_ DATA**</dt> <dt>13 (0xD)</dt> </dl>       | Der Treiber hat ein nicht unterstütztes Datenformat zurückgegeben.<br/>     |



 

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise, nur Windows 7 \[ Ultimate-Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\CIMV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
