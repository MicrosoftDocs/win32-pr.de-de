---
description: Schreibt eine Zeichenfolge in die angegebene Datenbank.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: SdbWriteStringTag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 942d7995e002f7f211a84c333d44e26531e361beec0adfaaa75ad7dc433ea3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075964"
---
# <a name="sdbwritestringtag-function"></a>SdbWriteStringTag-Funktion

Schreibt eine Zeichenfolge in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tTag* \[ In\]
</dt> <dd>

Das TAG für den Eintrag. Dieses TAG muss vom Typ **TAG \_ TYPE \_ STRINGREF sein.**

</dd> <dt>

*pwszData* \[ In\]
</dt> <dd>

Die auf NULL beendete Zeichenfolge. Dieser Parameter darf nicht **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE bei** Erfolg oder **FALSE bei** Einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




