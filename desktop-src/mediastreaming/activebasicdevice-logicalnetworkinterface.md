---
title: Activebasicdevice logicalnetworkinterface-Eigenschaft (playondevice. h)
description: Ruft die ID der logischen Netzwerkschnittstelle ab.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- Logicalnetworkinterface-Eigenschaft Medien Streaming-API
- Logicalnetworkinterface-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, logicalnetworkinterface (Eigenschaft)
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
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391837"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a>Activebasicdevice:: logicalnetworkinterface (Eigenschaft)

Ruft die ID der logischen Netzwerkschnittstelle ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **GUID** , die die ID der logischen Netzwerkschnittstelle angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Playondevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Playto Device. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

