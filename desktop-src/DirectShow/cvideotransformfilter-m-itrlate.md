---
description: Gibt an, wie spät die Stichproben am Renderer in Bezugszeit Einheiten eintreffen. Syntax.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Cvideotransformfilter:: m_itrLate Member (vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365526"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Cvideotransformfilter:: m \_ itrlate-Element

Gibt an, wie spät die Stichproben am Renderer in Bezugszeit Einheiten eintreffen. Syntax

## <a name="syntax"></a>Syntax


```C++
int m_itrLate;
```



## <a name="remarks"></a>Bemerkungen

Wenn der Filter eine Qualitäts Nachricht von Downstream empfängt, speichert er den oder bei Verzögerung-Wert in dieser Variablen. Beim Löschen des Filters wird dieser Wert aktualisiert, indem die Dauer der einzelnen Frames subtrahieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




