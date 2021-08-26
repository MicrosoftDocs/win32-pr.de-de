---
description: Ruft den Anzeigenamen des angegebenen TAGS ab.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString-Funktion
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
ms.openlocfilehash: 22ddb526e332b335e88ecc7aaa770615220f6b0dde838386093e2813fe964e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044840"
---
# <a name="sdbtagtostring-function"></a>SdbTagToString-Funktion

Ruft den Anzeigenamen des angegebenen TAGS ab.

## <a name="syntax"></a>Syntax


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tag* \[ In\]
</dt> <dd>

Das TAG.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen Zeiger auf die auf NULL endende Zeichenfolge oder "InvalidTag" zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Etikett**](tag.md)
</dt> </dl>

 

 




