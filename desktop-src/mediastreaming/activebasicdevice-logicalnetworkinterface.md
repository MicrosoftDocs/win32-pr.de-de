---
title: ActiveBasicDevice LogicalNetworkInterface-Eigenschaft (PlayToDevice.h)
description: Ruft die ID der logischen Netzwerkschnittstelle ab.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- LogicalNetworkInterface-Eigenschaft Media Streaming-API
- LogicalNetworkInterface-Eigenschaft Media Streaming-API, ActiveBasicDevice-Schnittstelle
- ActiveBasicDevice-Schnittstelle Medienstreaming-API, LogicalNetworkInterface-Eigenschaft
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ee3e2b23a43e29daf2438cee517220f895ad601607dbdc6a61497f8ef1afa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736386"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a>ActiveBasicDevice::LogicalNetworkInterface (Eigenschaft)

Ruft die ID der logischen Netzwerkschnittstelle ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **GUID,** die die ID der logischen Netzwerkschnittstelle angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

