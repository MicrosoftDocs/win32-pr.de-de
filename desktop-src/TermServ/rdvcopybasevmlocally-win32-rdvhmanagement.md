---
title: RdvCopyBaseVmLocally-Methode der Win32_RdvhManagement-Klasse
description: Kopiert einen lokalen virtuellen Basiscomputer auf einen angegebenen RDV-Hostserver (RemoteDesktopvirtualisierung).
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- RdvCopyBaseVmLocally-Remotedesktopdienste
- RdvCopyBaseVmLocally-Methode Remotedesktopdienste , Win32_RdvhManagement-Klasse
- Win32_RdvhManagement klasse Remotedesktopdienste , RdvCopyBaseVmLocally-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c260f8e9b659ac6e1316fc699ab832174a4aa0d0c24df26daecf5a4895ccd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118852625"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>RdvCopyBaseVmLocally-Methode der Win32 \_ RdvhManagement-Klasse

Kopiert einen lokalen virtuellen Basiscomputer auf einen angegebenen RDV-Hostserver (RemoteDesktopvirtualisierung).

## <a name="syntax"></a>Syntax


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BaseVmLocation* \[ In\]
</dt> <dd>

Der Basisspeicherort des virtuellen Computers.

</dd> <dt>

*FarmName* \[ In\]
</dt> <dd>

Der Name der Hostfarm, in die kopiert werden soll.

</dd> <dt>

*GoldCacheLocation* \[ In\]
</dt> <dd>

Der Speicherort des Goldcaches.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





