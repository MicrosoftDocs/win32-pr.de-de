---
description: Sperrt oder gibt die Medien frei.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Lockmedia-Methode der Msvm_DisketteDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869532"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a>Lockmedia-Methode der MSVM \_ diskettedrive-Klasse

Sperrt oder gibt die Medien frei.

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

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird einer der folgenden Werte zurückgegeben:

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

[**MSVM \_ diskettedrive**](msvm-diskettedrive.md)
</dt> </dl>

 

 




