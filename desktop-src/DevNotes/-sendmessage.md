---
description: Sendet die angegebene Meldung an ein Fenster oder an ein Fenster.
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
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370593"
---
# <a name="_sendmessage-function"></a>\_SendMessage-Funktion

\[Diese Funktion ist ein Wrapper über die **SendMessage** -Funktion. Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **SendMessage** direkt aufzurufen.\]

Sendet die angegebene Meldung an ein Fenster oder an ein Fenster. Siehe [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

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

 

 
