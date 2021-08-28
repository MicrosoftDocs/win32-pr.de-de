---
description: Die TAPI LINE DEVSPECIFICFEATURE-Nachricht wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem \_ Aufruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: LINE_DEVSPECIFICFEATURE (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c1ec56a41d6e57c6e090c9af682cb91c8ffdb891e376fcd9760ff1b51c5d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012530"
---
# <a name="line_devspecificfeature-message"></a>LINE \_ DEVSPECIFICFEATURE-Meldung

Die TAPI **LINE \_ DEVSPECIFICFEATURE-Nachricht** wird gesendet, um die Anwendung über gerätespezifische Ereignisse zu benachrichtigen, die in einer Zeile, Adresse oder einem Aufruf auftreten. Die Bedeutung der Nachricht und die Interpretation der Parameter sind gerätespezifisch.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für ein Liniengerät oder einen Anruf. Dies ist gerätespezifisch.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Gerätespezifisch.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Gerätespezifisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die **LINE \_ DEVSPECIFICFEATURE-Nachricht** wird von einem Dienstanbieter in Verbindung mit der [**lineDevSpecificFeature-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) verwendet. Seine Bedeutung ist gerätespezifisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




