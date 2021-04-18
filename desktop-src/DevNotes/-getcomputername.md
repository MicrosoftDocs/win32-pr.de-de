---
description: Ruft den Computernamen ab.
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: _GetComputerName-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371117"
---
# <a name="_getcomputername-function"></a>\_GetComputerName-Funktion

\[Diese Funktion ist ein Wrapper über die **GetComputerName** -Funktion. Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **GetComputerName** direkt aufrufen.\]

Ruft den Computernamen ab. Siehe [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).

## <a name="syntax"></a>Syntax


```C++
BOOL _GetComputerName(
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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
