---
description: Diese Funktionen bieten Unterstützung für die Implementierung der IUnknown-Schnittstelle in DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: COM-Hilfsfunktionen (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8558cd0d04258adf89cbacdd99952cf00c6d0aa5f24ee38cca2dceb4e5478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084340"
---
# <a name="com-helper-functions"></a>COM-Hilfsfunktionen

Diese Funktionen bieten Unterstützung für die Implementierung der **IUnknown-Schnittstelle** in DirectShow.



| Funktion                                               | Beschreibung                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DEKLARIEREN \_ VON IUNKNOWN**](declare-iunknown.md)          | Deklariert die drei Methoden der Basisschnittstelle für eine neue Schnittstelle. |
| [**Getinterface**](getinterface.md)                   | Ruft einen Schnittstellenzeiger auf den angeforderten Client ab.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Nicht delegierende Version der **IUnknown-Schnittstelle.**                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Lädt die Automatisierungs-DLL (OleAut32.dll).                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsfunktionen](utility-functions.md)
</dt> </dl>

 

 




