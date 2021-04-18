---
description: Sperrt oder entsperrt das Medium.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Lockmedia-Methode der Msvm_DiskDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361127"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a>Lockmedia-Methode der MSVM \_ diskdrive-Klasse

Sperrt oder entsperrt das Medium.

## <a name="syntax"></a>Syntax


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sperre* \[ in\]
</dt> <dd>

" **true** ", um die Medien zu sperren. **false** zum Freigeben der Medien.

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
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ diskdrive**](msvm-diskdrive.md)
</dt> </dl>

 

 




