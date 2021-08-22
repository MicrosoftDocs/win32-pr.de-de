---
description: Die LookupDwordSetString-Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert eines bezeichneten Sets entspricht.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: LookupDwordSetString-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b72f21d47001e2060c3b27daa80a584dcad77b55fd1df289a5bdb5476549cf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677230"
---
# <a name="lookupdwordsetstring-function"></a>LookupDwordSetString-Funktion

Die **LookupDwordSetString-Funktion** gibt die Zeichenfolge zurück, die dem angegebenen Wert eines bezeichneten Sets entspricht.

## <a name="syntax"></a>Syntax


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpSet* 
</dt> <dd>

Bezeichneter Satz, aus dem Sie die Bezeichnung des Werts extrahieren können.

</dd> <dt>

*Wert* 
</dt> <dd>

Der Wert eines bezeichneten Sets.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Zeichenfolge, die dem angegebenen Wert entspricht.

Wenn die Funktion nicht erfolgreich ist, der angegebene Wert nicht im Satz enthalten ist, ist der Rückgabewert **NULL.**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




