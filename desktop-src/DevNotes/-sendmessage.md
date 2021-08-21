---
description: Sendet die angegebene Meldung an ein Fenster oder ein Fenster.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: bdd8a072970d8e6fb5e9af082f6f220531539a1c0061a7688d48be30dd659a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572570"
---
# <a name="_sendmessage-function"></a>\_SendMessage-Funktion

\[Diese Funktion ist ein Wrapper für die **SendMessage-Funktion.** Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **SendMessage** direkt aufrufen.\]

Sendet die angegebene Meldung an ein Fenster oder ein Fenster. Weitere Informationen finden Sie unter [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

## <a name="syntax"></a>Syntax


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
