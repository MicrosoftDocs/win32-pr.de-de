---
description: Ruft den Benutzernamen ab.
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: _GetUserName-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351222"
---
# <a name="_getusername-function"></a>\_GetUserName-Funktion

\[Diese Funktion ist ein Wrapper über die **GetUsername** -Funktion. Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **GetUsername** direkt aufrufen.\]

Ruft den Benutzernamen ab. Siehe [**GetUsername**](/windows/win32/api/winbase/nf-winbase-getusernamea).

## <a name="syntax"></a>Syntax


```C++
BOOL _GetUserName(
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

[**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 
