---
description: Gibt eine Zeichenfolge an einer angegebenen Position innerhalb eines Blobs zurück.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Getstringfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484323"
---
# <a name="getstringfromblob-function"></a>Getstringfromblob-Funktion

Die **getstringfromblob** -Funktion gibt eine Zeichenfolge zurück, die sich an einer bestimmten Position innerhalb eines BLOB befindet.

## <a name="syntax"></a>Syntax


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Ein Handle für das BLOB.

</dd> <dt>

*pownername* \[ in\]
</dt> <dd>

Ein BLOB- **Besitzer** Abschnitt, in dem sich die Zeichenfolge befindet.

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Ein Abschnitt der BLOB- **Kategorie** , in dem sich die Zeichenfolge befindet.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Das **Tag** der angeforderten Zeichenfolge.

</dd> <dt>

*ppString* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die auf die zurückgegebene Zeichenfolge zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

Wenn die angegebenen **Besitzer**-, **Kategorie**-oder **Tagdaten** nicht vorhanden sind, gibt die Funktion den **nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Setstringinblob](setstringinblob.md)
</dt> <dt>

[Getboolfromblob](getboolfromblob.md)
</dt> <dt>

[Getclassidfromblob](getclassidfromblob.md)
</dt> <dt>

[Getdwordfromblob](getdwordfromblob.md)
</dt> <dt>

[Getmacaddressfromblob](getmacaddressfromblob.md)
</dt> <dt>

[Getnetworkinfofromblob](getnetworkinfofromblob.md)
</dt> <dt>

[Getnppaddressfilterfromblob](getnppaddressfilterfromblob.md)
</dt> <dt>

[Getnpppatternfilterfromblob](getnpppatternfilterfromblob.md)
</dt> <dt>

[Getnpptriggerfromblob](getnpptriggerfromblob.md)
</dt> <dt>

[Getstringsfromblob](getstringsfromblob.md)
</dt> </dl>

 

 




