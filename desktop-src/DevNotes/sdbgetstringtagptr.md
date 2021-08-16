---
description: Ruft die Zeichenfolgendaten für die angegebene TAGID ab.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: SdbGetStringTagPtr-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e14c499b5f23f342192ad42b72f8a4c29f8312adbf6bbcb8310ee182cd457f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404429"
---
# <a name="sdbgetstringtagptr-function"></a>SdbGetStringTagPtr-Funktion

Ruft die Zeichenfolgendaten für die angegebene **TAGID** ab.

## <a name="syntax"></a>Syntax


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tiWhich* \[ In\]
</dt> <dd>

Die **TAGID,** die den abzurufenden Zeichenfolgendaten entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen Zeiger auf die Zeichenfolgendaten oder **NULL** zurück, wenn die **TAGID** ungültig ist oder nicht vom Typ **TAG TYPE \_ \_ STRING** oder **TAG TYPE \_ \_ STRINGREF** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




