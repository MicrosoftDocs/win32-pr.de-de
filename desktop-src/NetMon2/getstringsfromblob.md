---
description: Verwendet sequenzielle Aufrufe, um alle Zeichen folgen innerhalb der angegebenen Bereiche abzurufen.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Getstringsfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958707"
---
# <a name="getstringsfromblob-function"></a>Getstringsfromblob-Funktion

Die **getstringsfromblob** -Funktion verwendet sequenzielle Aufrufe, um alle Zeichen folgen innerhalb der angegebenen Bereiche abzurufen.

## <a name="syntax"></a>Syntax


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Ein Handle für das BLOB.

</dd> <dt>

*prequestedownername* \[ in\]
</dt> <dd>

Ein Zeiger auf den Besitzer Abschnitt, von dem die Zeichenfolge abgeleitet werden soll.

</dd> <dt>

*prequestedcategoryname* \[ in\]
</dt> <dd>

Ein Zeiger auf den Kategorieabschnitt, von dem die Zeichenfolge abgeleitet werden soll.

</dd> <dt>

*prequestedtagname* \[ in\]
</dt> <dd>

Ein Zeiger auf das-Tag für die angeforderte Zeichenfolge.

</dd> <dt>

*ppreturnetdownername* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Variable, auf die verweist, wenn der **Besitzer** Name zurückgegeben wird.

</dd> <dt>

*ppreturnedcategoryname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Variable, die auf den Speicherort verweist, an dem der **Kategoriename** zurückgegeben wird.

</dd> <dt>

*ppreturnedtagname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Variable, auf die zeigt, wo der **Tagname** zurückgegeben wird.

</dd> <dt>

*ppreturnedstring* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Variable, auf die zeigt, wo der Zeichen folgen Name zurückgegeben wird.

</dd> <dt>

*prestartkey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Variable, in der die Neustart Taste angegeben und zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der das Problem angibt.

Wenn eine angegebene Kombination aus **Besitzer**, **Kategorie** und **Taginformationen** nicht vorhanden ist, ist der Rückgabewert **nmerr \_ BLOB \_ Entry \_ \_ nicht \_ vorhanden**.

Wenn das BLOB vollständig innerhalb der ursprünglich angegebenen Begrenzungen durchlaufen wird, gibt die Funktion den **nmerr- \_ \_ blobeintrag ist \_ \_ nicht \_ vorhanden** und der *prestartkey* -Parameter auf 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Beim ersten Aufrufen der **getstringsfromblob** -Funktion verweist der *prestartkey* -Parameter auf eine Variable, die den Wert 0 (null) enthält. Die *vorangefragten* Parameter können nur verwendet werden, wenn die Neustart Taste 0 (null) ist. In nachfolgenden Aufrufen, wenn *prestartkey* Werte ungleich NULL aufweist, werden die *vorangefragten* Parameter ignoriert. Beim ersten-Befehl können alle auf **null** zeigen, wodurch die Abfrage so eingerichtet wird, dass jeder Eintrag im BLOB zurückgegeben wird (einer pro nachfolgenden-Rückruf).

Durch die Angabe eines Besitzers werden die Zeichen folgen beschränkt, die nur an diesen Besitzer zurückgegeben Eine ähnliche Einschränkung gilt für Kategorien und Tags, mit der zusätzlichen Einschränkung: Wenn eine Kategorie angegeben wird, muss auch ein Besitzer angegeben werden, und wenn ein Tag angegeben wird, muss eine Kategorie (und somit ein Besitzer) angegeben werden.

Beim ersten Aufrufen von **getstringsfromblob** verweist *prestartkey* auf einen neuen Wert, der beim nächsten Aufrufen der-Funktion angegeben werden muss, um den nächsten Wert abzurufen.

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

[Getstringfromblob](getstringfromblob.md)
</dt> </dl>

 

 




