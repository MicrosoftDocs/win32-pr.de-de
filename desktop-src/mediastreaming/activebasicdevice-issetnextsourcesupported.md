---
title: Activebasicdevice issetnextsourcesupportiert-Eigenschaft (playondevice. h)
description: Ruft einen Wert ab, der angibt, ob das Festlegen der nächsten Quelle unterstützt wird.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- Issetnextsourcesupportiert-Eigenschaft Medien Streaming-API
- Issetnextsourcesupportiert-Eigenschaft Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, issetnextsourcesupportiert (Eigenschaft)
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346126"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a>Activebasicdevice:: issetnextsourcesupportiert (Eigenschaft)

Ruft einen Wert ab, der angibt, ob das Festlegen der nächsten Quelle unterstützt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **booleschen** Wert, der angibt, ob das Festlegen der nächsten Quelle unterstützt wird.

**true** , wenn das Festlegen der nächsten Quelle unterstützt wird. andernfalls **false**.

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

 

