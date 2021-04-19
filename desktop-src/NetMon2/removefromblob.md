---
description: Die removefromblob-Funktion löscht eine beliebige Ebene des BLOB-Eintrags (Besitzer, Kategorie oder Tag).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Removefromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346297"
---
# <a name="removefromblob-function"></a>Removefromblob-Funktion

Die **removefromblob** -Funktion löscht eine beliebige Ebene des BLOB-Eintrags (**Besitzer**, **Kategorie** oder **Tag**).

## <a name="syntax"></a>Syntax


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für das BLOB, aus dem ein Eintrag gelöscht wird.

</dd> <dt>

*pownername* \[ in\]
</dt> <dd>

Zeiger auf den Namen des **Besitzers** .

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Zeiger auf den **Kategorienamen** . Ein **null** -Parameterwert gibt an, dass der Aufrufer versucht, die angegebenen **Besitzer** Informationen und alle zugehörigen untergeordneten Einträge zu löschen. Beachten Sie, dass der *ptagname* -Parameter ebenfalls **null** sein muss, wenn der *pcategoryname* -Parameter den Wert **null** hat.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Zeiger auf den **Tagnamen** . Ein _ptagname_ -Wert von NULL gibt an, dass der Aufrufer versucht, die angegebene **Kategorie** und alle zugehörigen untergeordneten Einträge zu löschen. Wenn der Parameterwert nicht **null** ist, fragt der Aufrufer nur, dass die angegebenen **tageinträge** gelöscht werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




