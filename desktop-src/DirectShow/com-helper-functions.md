---
description: Diese Funktionen bieten Unterstützung für die Implementierung der IUnknown-Schnittstelle in DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: COM-Hilfsfunktionen (ComBase. h)
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
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370928"
---
# <a name="com-helper-functions"></a>COM-Hilfsfunktionen

Diese Funktionen bieten Unterstützung für die Implementierung der **IUnknown** -Schnittstelle in DirectShow.



| Funktion                                               | BESCHREIBUNG                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**\_IUnknown deklarieren**](declare-iunknown.md)          | Deklariert die drei Methoden der Basisschnittstelle für eine neue Schnittstelle. |
| [**GetInterface**](getinterface.md)                   | Ruft einen Schnittstellen Zeiger auf den angeforderten Client ab.               |
| [**Inondelegatingunknown**](inondelegatingunknown.md) | Nicht delegierende Version der **IUnknown** -Schnittstelle.                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Lädt die Automation-dll (OleAut32.dll).                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsfunktionen](utility-functions.md)
</dt> </dl>

 

 




