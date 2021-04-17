---
description: Ruft den anzeigen amen des angegebenen Tags ab.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Sdbtagto String-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483123"
---
# <a name="sdbtagtostring-function"></a>Sdbtagto String-Funktion

Ruft den anzeigen amen des angegebenen Tags ab.

## <a name="syntax"></a>Syntax


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tag* \[ in\]
</dt> <dd>

Das-Tag.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt einen Zeiger auf die NULL-terminierte Zeichenfolge oder "invalidtag" zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tag**](tag.md)
</dt> </dl>

 

 




