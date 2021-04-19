---
description: Sendet eingehende gesendete Nachrichten, überprüft die Thread Meldungs Warteschlange auf eine gesendete Nachricht und ruft die Nachricht (sofern vorhanden) ab.
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
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356363"
---
# <a name="_peekmessage-function"></a>\_Peer Message-Funktion

\[Diese Funktion ist ein Wrapper über die Funktion " **Peer Message** ". Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten " **Peer-Message** " direkt aufrufen.\]

Sendet eingehende gesendete Nachrichten, überprüft die Thread Meldungs Warteschlange auf eine gesendete Nachricht und ruft die Nachricht (sofern vorhanden) ab. Siehe " [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea)".

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

 

 
