---
title: Activebasicdevice physicalnetworkinterface-Eigenschaft (playondevice. h)
description: Ruft die ID der physischen Netzwerkschnittstelle ab.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- Physicalnetworkinterface-Eigenschaft Medien Streaming-API
- Physicalnetworkinterface-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, physicalnetworkinterface (Eigenschaft)
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477367"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>Activebasicdevice::P hysicalnetworkinterface-Eigenschaft

Ruft die ID der physischen Netzwerkschnittstelle ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **GUID** , die die ID der physischen Netzwerkschnittstelle angibt.

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

 

