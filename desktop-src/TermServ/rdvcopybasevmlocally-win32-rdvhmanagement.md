---
title: Rdvcopybasevmlokal-Methode der Win32_RdvhManagement-Klasse
description: Kopiert eine lokale virtuelle Basismaschine auf einen angegebenen RDV-Host Server (Remote Desktop Virtualization).
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Rdvcopybasevmlokal-Methode Remotedesktopdienste
- Rdvcopybasevmlokal-Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvcopybasevmlokal-Methode
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
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392168"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a>Rdvcopybasevmlokal-Methode der Win32 \_ rdvhmanagement-Klasse

Kopiert eine lokale virtuelle Basismaschine auf einen angegebenen RDV-Host Server (Remote Desktop Virtualization).

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

*Basevmlocation* \[ in\]
</dt> <dd>

Der Speicherort der virtuellen Basismaschine.

</dd> <dt>

*Farmname* \[ in\]
</dt> <dd>

Der Name der Host Farm, in die kopiert werden soll.

</dd> <dt>

*Goldcacheloation* \[ in\]
</dt> <dd>

Der Speicherort des Gold Caches.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>"Zvmhost. mof"</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdvhmanagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





