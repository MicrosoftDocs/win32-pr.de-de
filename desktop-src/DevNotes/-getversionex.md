---
description: Ruft Informationen zur Betriebssystemversion ab.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 2e3047edfaf2dabe591172dd3ca292f41aeefa90774231b417f5405e3aeb18c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956289"
---
# <a name="_getversionex-function"></a>\_GetVersionEx-Funktion

\[Diese Funktion ist ein Wrapper für die **GetVersionEx-Funktion.** Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Anwendungen sollten **GetVersionEx direkt** aufrufen.\]

Ruft Informationen zur Betriebssystemversion ab. Weitere Informationen [**finden Sie unter GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).

## <a name="syntax"></a>Syntax


```C++
BOOL _GetVersionEx(
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

[**Getversionex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
