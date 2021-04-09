---
description: Sperrt und entsperrt die Medien in einem Remote fähigen Zugriffsgerät.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Lockmedia-Methode der CIM_MediaAccessDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050671"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a>Lockmedia-Methode der CIM \_ mediaaccessdevice-Klasse

Sperrt und entsperrt die Medien in einem Remote fähigen Zugriffsgerät.

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

Wenn der Wert **true** ist, wird das Medium gesperrt. Wenn **false**, wird das Medium von freigegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

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

[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




