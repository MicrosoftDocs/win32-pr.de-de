---
description: Legt eine Zeichenfolge an einer angegebenen Position innerhalb eines BLOBs fest.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Setstringinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214742"
---
# <a name="setstringinblob-function"></a>Setstringinblob-Funktion

Die **setstringinblob** -Funktion legt eine Zeichenfolge an einer bestimmten Position innerhalb eines BLOBs fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
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

Ein Zeiger auf den **Besitzer** Abschnitt des BLOBs, in dem die Zeichenfolge festgelegt ist.

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Ein Zeiger auf den **Kategorieabschnitt** des BLOBs, in dem die Zeichenfolge festgelegt ist.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Ein Zeiger auf das **Tag** der angeforderten Zeichenfolge.

</dd> <dt>

*pstring* \[ in\]
</dt> <dd>

Ein Zeiger auf die Variable, in der ein Zeiger auf die Zeichenfolge zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der das Problem angibt.

Wenn die angegebenen **Besitzer**-, **Kategorie**-oder **Taginformationen** nicht vorhanden sind, ist der Rückgabewert nmerr \_ BLOB \_ Entry \_ \_ nicht \_ vorhanden.

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

[Getstringfromblob](getstringfromblob.md)
</dt> <dt>

[Setboolinblob](setboolinblob.md)
</dt> <dt>

[Setclassidinblob](setclassidinblob.md)
</dt> <dt>

[Setdwordinblob](setdwordinblob.md)
</dt> <dt>

[Setmacaddressinblob](setmacaddressinblob.md)
</dt> <dt>

[Setnetworkinfoinblob](setnetworkinfoinblob.md)
</dt> <dt>

[Setnppaddressfilterinblob](setnppaddressfilterinblob.md)
</dt> <dt>

[Setnpppatternfilterinblob](setnpppatternfilterinblob.md)
</dt> <dt>

[Setnpptriggerinblob](setnpptriggerinblob.md)
</dt> </dl>

 

 




