---
description: Sendet eingehende gesendete Nachrichten, überprüft die Threadnachrichtenwarteschlange auf eine gesendete Nachricht und ruft die Nachricht ab (sofern vorhanden).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2a2fbfcf1903fcafba77227a6b2b9f51b9c6a45ef2e8a20f7482db1f3ec2a7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538890"
---
# <a name="_peekmessage-function"></a>\_PeekMessage-Funktion

\[Diese Funktion ist ein Wrapper für die **PeekMessage-Funktion.** Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **PeekMessage** direkt aufrufen.\]

Sendet eingehende gesendete Nachrichten, überprüft die Threadnachrichtenwarteschlange auf eine gesendete Nachricht und ruft die Nachricht ab (sofern vorhanden). Weitere Informationen finden Sie unter [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

## <a name="syntax"></a>Syntax


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
