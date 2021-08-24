---
description: Die BuildINIPath-Funktion gibt einen vollqualifizierten Pfad zu einer INI-Datei zurück, die den von Ihnen eingeben Informationen entspricht.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: BuildINIPath-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b75df338142ab0ec97db3e60cbba1b5f68df3e0e67947d4c13cdccccd409bdf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744691"
---
# <a name="buildinipath-function"></a>BuildINIPath-Funktion

Die **BuildINIPath-Funktion** gibt einen vollqualifizierten Pfad zu einer INI-Datei zurück, die den von Ihnen eingeben Informationen entspricht.

## <a name="syntax"></a>Syntax


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FullPath* 
</dt> <dd>

Puffer, der den vollqualifizierten INI-Dateinamen empfängt.

</dd> <dt>

*IniFileName* 
</dt> <dd>

Name der INI-Datei (der vollständige Dateiname abzüglich der Dateierweiterung).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den vollqualifizierten INI-Dateinamen.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Der Pfad, den diese Funktion zurückgibt, ist ein vollqualifizierter Pfad zu einer INI-Datei, die den von Ihnen eingeben Informationen entspricht. Wenn Sie beispielsweise XNS oder TCP eingeben, generiert die Funktion einen Pfad zu Xns.ini oder Tcp.ini bzw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




