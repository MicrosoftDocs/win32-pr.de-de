---
description: Gibt den Offset eines angegebenen Protokolls im Frame zurück.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Getprotocolstarttffset-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353018"
---
# <a name="getprotocolstartoffset-function"></a>Getprotocolstartffset-Funktion

Die **getprotocolstartoffset** -Funktion gibt den Offset eines angegebenen Protokolls im Frame zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* 
</dt> <dd>

Ein Handle für den Frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Der Protokoll Name, z. b. TCP.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, handelt es sich bei dem Rückgabewert um einen **DWORD** -Offset bis zum Anfang des gesuchten Protokolls für einen Rückgabewert von NULL gibt an, dass das Protokoll das erste Protokoll im Frame ist.

Wenn die Funktion nicht erfolgreich ist, befindet sich das Protokoll nicht im Frame, der Rückgabewert ist-1.

## <a name="remarks"></a>Bemerkungen

Wenn das Handle an einen Frame übergeben wird, gibt diese Funktion den Offset an ein angegebenes Protokoll im Frame zurück. Um z. b. zu ermitteln, ob es sich bei dem Frame um einen DNS-Frame handelt, benötigt der DNS-Parser die Portadresse des TCP-Protokolls. Der DNS-Parser würde diese Funktion mit TCP als *ProtocolName* -Wert bezeichnen. Wenn der Frame vom TCP-Protokoll erkannt wird, wird der **Wort** Offset vom Anfang des Frames bis zum Anfang des TCP-Frames zurückgegeben. Wenn kein TCP-Protokoll vorhanden ist, ist der Rückgabewert 0 (null).

Diese Funktion findet den Anfang eines Protokolls in einem Frame.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




