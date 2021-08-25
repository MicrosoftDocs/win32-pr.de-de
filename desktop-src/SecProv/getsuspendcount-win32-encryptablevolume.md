---
description: Ruft ab, wie oft BitLocker angehalten wurde.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: GetSuspendCount-Methode der Win32_EncryptableVolume -Klasse (Activdbg.h)
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
ms.openlocfilehash: 468bd6cdc8f3df7efba26997fd76b0724d3e4cc5da552275dad5201adc469f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906350"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>GetSuspendCount-Methode der Win32 \_ EncryptableVolume-Klasse

Die **GetSuspendCount-Methode** der [**Win32 \_ EncryptableVolume-Klasse**](win32-encryptablevolume.md) ruft die Anzahl von Neustarts ab, bevor der Schutz automatisch fortgesetzt wird.

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
| <dl> <dt>**FEHLER \_ WIRD NICHT \_ UNTERSTÜTZT**</dt> </dl> | Wird zurückgegeben, wenn das Volume nicht angehalten wird oder kein Betriebssystem-Volume ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode gilt nur für das Betriebssystem-Volume und nur, wenn es tatsächlich zu diesem Zeitpunkt angehalten wird. Wenn das Volume nicht angehalten wird oder kein Betriebssystem-Volume ist, wird **ERROR \_ NOT \_ SUPPORTED** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 Enterprise, nur Windows 8 Pro \[ Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\CimV2-Stammsicherheit \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| Header<br/>                   | <dl> <dt>Activdbg.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




