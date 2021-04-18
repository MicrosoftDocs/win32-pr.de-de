---
description: Die buildinipath-Funktion gibt einen voll qualifizierten Pfad zu einer INI-Datei zurück, die den von Ihnen eingegebenen Informationen entspricht.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Buildinipath-Funktion (Netmon. h)
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
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368023"
---
# <a name="buildinipath-function"></a>Buildinipath-Funktion

Die **buildinipath** -Funktion gibt einen voll qualifizierten Pfad zu einer INI-Datei zurück, die den von Ihnen eingegebenen Informationen entspricht.

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

Puffer, der den voll qualifizierten Namen der INI-Datei empfängt.

</dd> <dt>

*Dateiname* 
</dt> <dd>

Name der INI-Datei (der vollständige Dateiname abzüglich der Dateinamenerweiterung).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den voll qualifizierten Namen der INI-Datei.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Der von dieser Funktion zurückgegebene Pfad ist ein voll qualifizierter Pfad zu einer INI-Datei, die den von Ihnen eingegebenen Informationen entspricht. Wenn Sie z. b. XNS oder TCP eingeben, generiert die Funktion einen Pfad zu Xns.ini bzw. Tcp.ini.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




