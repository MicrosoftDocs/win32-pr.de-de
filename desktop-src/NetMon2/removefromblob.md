---
description: Die RemoveFromBlob-Funktion löscht alle Ebenen von BLOB-Einträgen (Besitzer, Kategorie oder Tag).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: RemoveFromBlob-Funktion (Netmon.h)
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
ms.openlocfilehash: 09c9c7f5ada320f33d38cd9e935add7e47721c554fbeed11c35a1b73248d963c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063690"
---
# <a name="removefromblob-function"></a>RemoveFromBlob-Funktion

Die **RemoveFromBlob-Funktion** löscht alle Ebenen von BLOB-Einträgen **(Besitzer,** **Kategorie** oder **Tag**).

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

*hBlob* \[ In\]
</dt> <dd>

Handle für das BLOB, aus dem ein Eintrag gelöscht wird.

</dd> <dt>

*pOwnerName* \[ In\]
</dt> <dd>

Zeiger auf den **Besitzernamen.**

</dd> <dt>

*pCategoryName* \[ In\]
</dt> <dd>

Zeiger auf den **Kategorienamen.** Ein **NULL-Parameterwert** gibt an, dass der Aufrufer versucht, die angegebenen **Besitzerinformationen** und alle untergeordneten Einträge zu löschen. Beachten Sie Folgendes: Wenn der *pCategoryName-Parameterwert* **NULL** ist, muss der *pTagName-Parameter* auch **NULL** sein.

</dd> <dt>

*pTagName* \[ In\]
</dt> <dd>

Zeiger auf den **Tagnamen.** Ein _NULL-pTagName-Wert_ gibt an, dass der Aufrufer versucht, die angegebene **Kategorie** und alle untergeordneten Einträge zu löschen.  Wenn der Parameterwert nicht **NULL** ist, fordert der Aufrufer nur an, dass die angegebenen **Tageinträge** gelöscht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




