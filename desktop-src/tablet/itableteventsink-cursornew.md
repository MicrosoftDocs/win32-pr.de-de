---
description: Tritt ein, wenn dem System ein neuer Stift hinzugefügt wird.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: ITabletEventSink::CursorNew-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 989c61d7f9ae4ce6b4f3136887d087605c61eff759bac7664a84388d2b509b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857139"
---
# <a name="itableteventsinkcursornew-method"></a>ITabletEventSink::CursorNew-Methode

Tritt ein, wenn dem System ein neuer Stift hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tcid* \[ In\]
</dt> <dd>

Der Bezeichner des Tablet-Kontexts, in dem der neue Tablettstift hinzugefügt wurde.

</dd> <dt>

*Cid* 
</dt> <dd>

Der Bezeichner des neuen Stiftobjekts.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




