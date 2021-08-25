---
description: Ruft die Attributdaten für die angegebene Datei ab.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a75dd64bfbeaf027839c63227c594ada7602101d059cbbd9d10deb085152918d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103650"
---
# <a name="sdbgetfileattributes-function"></a>SdbGetFileAttributes-Funktion

Ruft die Attributdaten für die angegebene Datei ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpwszFileName* \[ In\]
</dt> <dd>

Der Pfad zur Datei.

</dd> <dt>

*ppAttrInfo* \[ out\]
</dt> <dd>

Ein Array von [**ATTRINFO-Strukturen,**](attrinfo.md) die die Attributdaten enthalten.

</dd> <dt>

*lpdwAttrCount* \[ out\]
</dt> <dd>

Die Anzahl der Attribute.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE bei** Erfolg oder **FALSE bei** Einem Fehler zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie mit den Daten fertig sind, geben Sie sie mithilfe der [**Funktion SdbFreeFileAttributes**](sdbfreefileattributes.md) frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




