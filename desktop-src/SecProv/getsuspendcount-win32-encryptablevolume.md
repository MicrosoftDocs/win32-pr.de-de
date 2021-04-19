---
description: Ruft ab, wie oft BitLocker angehalten wurde.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Getsuspendcount-Methode der Win32_EncryptableVolume-Klasse (activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373222"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Getsuspendcount-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **getsuspendcount** -Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " Ruft die Anzahl der Neustarts ab, bevor der Schutz automatisch fortgesetzt wird.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SuspendCount* 
</dt> <dd>

Ein ganzzahliger Wert zwischen 0 und 15.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode                                                                                          | Beschreibung                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Die Methode war erfolgreich.<br/>                                      |
| <dl> <dt>**Fehler \_ nicht \_ unterstützt**</dt> </dl> | Wird zurückgegeben, wenn das Volume nicht angehalten wird oder kein Betriebssystem Volume ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gilt nur für das Betriebssystem Volume und nur, wenn Sie zu diesem Zeitpunkt tatsächlich angehalten wird. Wenn das Volume nicht angehalten wird oder kein Betriebssystem Volume ist, wird ein Fehler zurückgegeben, der **\_ nicht \_ unterstützt** wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 Enterprise, Windows 8 pro \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| Header<br/>                   | <dl> <dt>Activdbg. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




