---
description: Gibt die angegebenen Dateiattributdaten frei.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7e99180198f8f23ba6b6872502710b2af28aaff3999a9f315c33ef2d1874d987
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103670"
---
# <a name="sdbfreefileattributes-function"></a>SdbFreeFileAttributes-Funktion

Gibt die angegebenen Dateiattributdaten frei.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileAttributes* \[ In\]
</dt> <dd>

Eine [**ATTRINFO-Struktur,**](attrinfo.md) die von der [**SdbGetFileAttributes-Funktion zurückgegeben**](sdbgetfileattributes.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE bei** Erfolg oder **FALSE bei** Einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




