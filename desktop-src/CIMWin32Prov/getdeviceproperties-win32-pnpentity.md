---
description: Ruft die angegebenen Eigenschaften dieses Plug & Play ab.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: GetDeviceProperties-Methode der Win32_PnPEntity Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 855c3c0644d8c7b5c5300c8d12d5a6f98073a4511f8d0d65f4058da7fb9d0f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077510"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>GetDeviceProperties-Methode der Win32 \_ PnPEntity-Klasse

Ruft die angegebenen Eigenschaften dieses Plug & Play ab.

## <a name="syntax"></a>Syntax


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*devicePropertyKeys* \[ in, optional\]
</dt> <dd>

Die zurück zu gebenden Eigenschaften.

</dd> <dt>

*deviceProperties* \[ out\]
</dt> <dd>

Die angeforderten Eigenschaften in den entsprechenden Untertypen der [**abstrakten Win32 \_ PnPDeviceProperty-Klasse.**](win32-pnpdeviceproperty.md)

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)
</dt> </dl>

 

 




