---
description: 'LockMedia-Methode der Msvm_DVDDrive-Klasse: Sperrt oder gibt die Medien frei.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: LockMedia-Methode der Msvm_DVDDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e86ef975d872f0fd86922f25f9752fda7508a037e293db85245ef6b1384a1570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525320"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a>LockMedia-Methode der Msvm \_ DVDDrive-Klasse

Sperrt oder gibt die Medien frei.

## <a name="syntax"></a>Syntax


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sperren* \[ In\]
</dt> <dd>

**TRUE,** um die Medien zu sperren; **FALSE,** um die Medien freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück:

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ DVDDrive**](msvm-dvddrive.md)
</dt> </dl>

 

 




