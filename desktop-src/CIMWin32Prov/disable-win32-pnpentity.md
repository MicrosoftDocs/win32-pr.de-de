---
description: Deaktiviert dieses Plug & Play Gerät.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Deaktivieren der Methode der Win32_PnPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523395"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a>Deaktivieren der Methode der Win32- \_ pnptity-Klasse

Deaktiviert dieses Plug & Play Gerät.

## <a name="syntax"></a>Syntax


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*neubootbedarf* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob ein Neustart erforderlich ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ pnptity**](win32-pnpentity.md)
</dt> </dl>

 

 




