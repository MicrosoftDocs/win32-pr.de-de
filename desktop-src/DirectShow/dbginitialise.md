---
description: Die dbginitialise-Funktion initialisiert die Debug-Bibliothek. Wird in Einzelhandels Builds ignoriert.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Dbginitialise-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351300"
---
# <a name="dbginitialise-function"></a>Dbginitialise-Funktion

Die **dbginitialise** -Funktion initialisiert die Debug-Bibliothek. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinst* 
</dt> <dd>

Handle für die Modul Instanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

In einer ausführbaren Datei wird diese Methode aufgerufen, bevor die DirectShow-Debugfunktionen verwendet werden. Bevor die ausführbare Datei beendet wird, müssen Sie die [**dbgend**](dbgterminate.md) -Funktion zum Bereinigen der Debugbibliothek aufzurufen.

In einer DLL, die mit der Basisklassen Bibliothek verknüpft ist ("straumbase. lib"), ist es nicht erforderlich, diese Funktion aufzurufen. Die-Funktion wird automatisch aufgerufen, wenn die dll geladen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




