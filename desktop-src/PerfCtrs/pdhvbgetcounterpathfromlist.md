---
description: Die PdhVbGetCounterPathFromList-Funktion kopiert den Indikatorpfad, auf den der Index-Parameter verweist, aus einer Vom Benutzer erstellten Indikatorpfadliste aus dem letzten Aufruf der PdhVbCreateCounterPathList-Funktion.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 85760bbcdcc81204340004304be1f0c14bf9bcbbbd7a5b59eebf47a25f7b15c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033780"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>PdhVbGetCounterPathFromList-Funktion

Die **PdhVbGetCounterPathFromList-Funktion** kopiert den Indikatorpfad, auf den der *Index-Parameter* verweist, aus einer Vom Benutzer erstellten Indikatorpfadliste aus dem letzten Aufruf der [**PdhVbCreateCounterPathList-Funktion.**](pdhvbcreatecounterpathlist.md)

> [!IMPORTANT]
> Die funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der unter [Leistungsindikatorfunktionen beschriebenen Funktionen.](performance-counters-functions.md)

Funktion PdhVbGetCounterPathFromList( \_ ByVal Index so \_ long, ByVal Buffer as String, \_ ByVal BufferLength as long \_ ) as long

## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Index des abzurufenden Indikatorpfads. Dies muss ein Wert sein, der größer oder gleich 1 und kleiner oder gleich dem Wert ist, der von der [**PdhVbCreateCounterPathList-Funktion zurückgegeben**](pdhvbcreatecounterpathlist.md) wird.

</dd> <dt>

*Buffer* 
</dt> <dd>

Dimensionierte und initialisierte Zeichenfolge, die den Indikatorpfad erhält, der dem Wert des Index-Parameters entspricht.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Maximale Anzahl von Zeichen, die in die Zeichenfolge passen, auf die buffer verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die Anzahl der in Buffer kopierten Zeichen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




