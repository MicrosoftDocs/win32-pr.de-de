---
description: Ruft die angegebenen Eigenschaften dieses Plug & Play Geräts ab.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Getdeviceproperties-Methode der Win32_PnPEntity-Klasse
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
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041397"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Getdeviceproperties-Methode der Win32 \_ pnptity-Klasse

Ruft die angegebenen Eigenschaften dieses Plug & Play Geräts ab.

## <a name="syntax"></a>Syntax


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*devicepropertykeys* \[ in, optional\]
</dt> <dd>

Die zurück zugebende Eigenschaften.

</dd> <dt>

*deviceproperties* \[ vorgenommen\]
</dt> <dd>

Die angeforderten Eigenschaften in den entsprechenden Untertypen der [**Win32- \_ pnpdeviceproperty**](win32-pnpdeviceproperty.md) abstract-Klasse.

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

 

 




