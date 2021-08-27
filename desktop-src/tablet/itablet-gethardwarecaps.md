---
description: Gibt einen Wert zurück, der die Funktionen der Tabletthardware darstellt.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: ITablet::GetHardwareCaps-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 6faa286a95c27556427ed62dfebd6b16496b22b2e55263661f529709d546656b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031908"
---
# <a name="itabletgethardwarecaps-method"></a>ITablet::GetHardwareCaps-Methode

Gibt einen Wert zurück, der die Funktionen der Tabletthardware darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwCaps* \[ out\]
</dt> <dd>

Bitflags, die die Funktionen der Tablet-Hardware darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Der *pdwCaps-Parameter* ist ein Satz von Bitflags, die Tablet-Hardwarefunktionen beschreiben. In der folgenden Tabelle werden diese Flags beschrieben.



| Flagname                         | Wert                 | Beschreibung                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| THWC \_ INTEGRATED<br/>       | 0x00000001<br/> | Gibt an, dass die Anzeige und der Digitizer dieselbe Oberfläche gemeinsam haben.<br/>                                                    |
| THWC \_ CSR \_ MUST \_ TOUCH<br/> | 0x00000002<br/> | Gibt an, dass sich der Cursor in physischem Kontakt mit dem Gerät befindet, um die Position zu melden.<br/>                           |
| THWC \_ HARD \_ PROXIMITY<br/>  | 0x00000004<br/> | Gibt an, dass das Gerät Ereignisse generieren kann, wenn der Cursor in den physischen Erkennungsbereich eintritt und diesen verlässt.<br/> |
| THWC \_ PHYSID \_ CSRS<br/>     | 0x00000008<br/> | Gibt an, dass das Gerät den aktiven Cursor in der Hardware eindeutig identifizieren kann.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> </dl>

 

 




