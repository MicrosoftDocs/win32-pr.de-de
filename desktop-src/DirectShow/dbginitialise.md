---
description: Die DbgInitialise-Funktion initialisiert die Debugbibliothek. Wird in Einzelhandels-Builds ignoriert.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: DbgInitialise-Funktion (Wxdebug.h)
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
ms.openlocfilehash: 13aad8d0214c65c01237c8e74548c3915af9287c935b53e33c6d229b2da5b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654215"
---
# <a name="dbginitialise-function"></a>DbgInitialise-Funktion

Die **DbgInitialise-Funktion** initialisiert die Debugbibliothek. Wird in Einzelhandels-Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hInst* 
</dt> <dd>

Handle für die Modulinstanz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode in einer ausführbaren Datei auf, bevor Sie die DirectShow-Debugmöglichkeiten verwenden. Rufen Sie vor dem Beenden der ausführbaren Datei die [**DbgTerminate-Funktion**](dbgterminate.md) auf, um die Debugbibliothek zu bereinigt.

In einer DLL, die mit der Basisklassenbibliothek (Strmbase.lib) verknüpft ist, muss diese Funktion nicht aufrufen werden. Die Funktion wird automatisch aufgerufen, wenn die DLL geladen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




