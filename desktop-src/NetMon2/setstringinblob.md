---
description: Legt eine Zeichenfolge an einer bestimmten Position in einem BLOB fest.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: SetStringInBlob-Funktion (Netmon.h)
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
ms.openlocfilehash: 293aabf86769a8cfa678df79a04b5158b9c1d19c80d660b144c4a33cbf32c56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363679"
---
# <a name="setstringinblob-function"></a>SetStringInBlob-Funktion

Die **SetStringInBlob-Funktion** legt eine Zeichenfolge an einer bestimmten Position in einem BLOB fest.

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

*hBlob* \[ In\]
</dt> <dd>

Ein Handle für das BLOB.

</dd> <dt>

*pOwnerName* \[ In\]
</dt> <dd>

Ein Zeiger auf den **Abschnitt Besitzer** des BLOB, in dem die Zeichenfolge festgelegt ist.

</dd> <dt>

*pCategoryName* \[ In\]
</dt> <dd>

Ein Zeiger auf den Abschnitt **Category** des BLOB, in dem die Zeichenfolge festgelegt ist.

</dd> <dt>

*pTagName* \[ In\]
</dt> <dd>

Ein Zeiger auf das **Tag** der angeforderten Zeichenfolge.

</dd> <dt>

*pString* \[ In\]
</dt> <dd>

Ein Zeiger auf die Variable, in der ein Zeiger auf die Zeichenfolge zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der das Problem angibt.

Wenn die **angegebenen** Besitzer-, **Kategorie-** oder **Taginformationen** nicht vorhanden sind, lautet der Rückgabewert NMERR \_ BLOB ENTRY DOES NOT \_ \_ \_ \_ EXIST.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> </dl>

 

 




