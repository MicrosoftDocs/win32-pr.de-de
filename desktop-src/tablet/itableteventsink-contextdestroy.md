---
description: Tritt ein, wenn ein Tabletkontext zerstört wird.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: ITabletEventSink::ContextDestroy-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 6e220b812c046420d8d0fa057bf2defddd9b50666665ab2ccdfdc5df7aa46438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883500"
---
# <a name="itableteventsinkcontextdestroy-method"></a>ITabletEventSink::ContextDestroy-Methode

Tritt ein, wenn ein Tabletkontext zerstört wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tcid* \[ In\]
</dt> <dd>

Der Bezeichner des tablet-Kontexts, der zerstört wird.

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

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




