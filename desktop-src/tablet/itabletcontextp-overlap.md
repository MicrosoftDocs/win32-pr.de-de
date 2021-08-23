---
description: Verschiebt einen Tablet-Kontext an den Vorder- oder Hintergrund der Eingabewarteschlange.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: ITabletContextP::Overlap-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: ec8b462f2d06e1613c32b795af1793776cafddd6a3531ac6a0b5385f3d3e5128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712240"
---
# <a name="itabletcontextpoverlap-method"></a>ITabletContextP::Overlap-Methode

Verschiebt einen Tablet-Kontext an den Vorder- oder Hintergrund der Eingabewarteschlange.

## <a name="syntax"></a>Syntax


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bTop* \[ In\]
</dt> <dd>

Gibt an, ob der Tablet-Kontext an den anfang oder unteren Rand der Eingabewarteschlange verschoben werden soll.

</dd> <dt>

*pdwtcid* \[ out\]
</dt> <dd>

Der Tablet-Kontextbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletContextP-Schnittstelle**](itabletcontextp.md)
</dt> </dl>

 

 




