---
description: Gibt einen Wert zurück, der die Funktionen der Tablet-Hardware darstellt.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'ITablet:: gethardwarecaps-Methode'
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
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867723"
---
# <a name="itabletgethardwarecaps-method"></a>ITablet:: gethardwarecaps-Methode

Gibt einen Wert zurück, der die Funktionen der Tablet-Hardware darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwcaps* \[ vorgenommen\]
</dt> <dd>

Bitflags, die die Funktionen der Tablet-Hardware darstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der *pdwcaps* -Parameter ist ein Satz von Bitflags, die Tablet-Hardwarefunktionen beschreiben. In der folgenden Tabelle werden diese Flags beschrieben.



| FlagName                         | Wert                 | BESCHREIBUNG                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Integration in thwc \_<br/>       | 0x00000001<br/> | Gibt an, dass die Anzeige und der Digitalisierer dieselbe Oberfläche verwenden.<br/>                                                    |
| thwc- \_ CSR \_ muss \_ berühren<br/> | 0x00000002<br/> | Gibt an, dass sich der Cursor in einem physischen Kontakt mit dem Gerät befinden muss, um die Position zu melden.<br/>                           |
| harte thwc- \_ \_ Nähe<br/>  | 0x00000004<br/> | Gibt an, dass das Gerät Ereignisse generieren kann, wenn der Cursor in den Bereich physischer Erkennungsbereich wechselt und diesen verlässt.<br/> |
| thwc \_ physid \_ csrs<br/>     | 0x00000008<br/> | Gibt an, dass das Gerät den aktiven Cursor in der Hardware eindeutig identifizieren kann.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> </dl>

 

 




