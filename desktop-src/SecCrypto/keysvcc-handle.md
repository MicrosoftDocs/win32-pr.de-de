---
description: Der KEYSVCC \_ HANDLE-Datentyp definiert ein Schlüsseldiensthand handle. Ein KEYSVCC \_ HANDLE-Handle wird von den Funktionen RKeyOpenKeyService und RKeyCloseKeyService verwendet.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32e34285c6291cb7cb87aeb9095e5261b43999b0eefa82e33704719e7673f1b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515950"
---
# <a name="keysvcc_handle"></a>KEYSVCC \_ HANDLE

Der **KEYSVCC \_ HANDLE-Datentyp** definiert ein Schlüsseldiensthand handle. Ein **KEYSVCC \_ HANDLE-Handle** wird von den [**Funktionen RKeyOpenKeyService**](rkeyopenkeyservice.md) und [**RKeyCloseKeyService**](rkeyclosekeyservice.md) verwendet.


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




