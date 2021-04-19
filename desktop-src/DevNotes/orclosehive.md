---
description: Schließt die angegebene Offline Registrierungs Struktur und gibt für die Hive zugeordnete Arbeitsspeicher frei.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Orclosehive-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370297"
---
# <a name="orclosehive-function"></a>Orclosehive-Funktion

Schließt die angegebene Offline Registrierungs Struktur und gibt für die Hive zugeordnete Arbeitsspeicher frei.

## <a name="syntax"></a>Syntax


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für den Stamm Schlüssel der zu schließenden Offline Registrierungs Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="remarks"></a>Bemerkungen

Die **orclosehive** -Funktion gibt den gesamten Arbeitsspeicher frei, der von den Offline Registrierungsfunktionen für die angegebene Hive reserviert wurde.

Um Änderungen an der Struktur beizubehalten, rufen Sie die [**orsavehive**](orsavehive.md) -Funktion auf, bevor Sie **orclosehive** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Oropenhive**](oropenhive.md)
</dt> <dt>

[**Orsavehive**](orsavehive.md)
</dt> </dl>

 

 
