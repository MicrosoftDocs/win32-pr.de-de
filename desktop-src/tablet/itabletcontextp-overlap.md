---
description: Verschiebt einen Tablet-Kontext an die Vorder-oder Rückseite der Eingabe Warteschlange.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Itabletcontextp:: überlappungsmethode'
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
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359472"
---
# <a name="itabletcontextpoverlap-method"></a>Itabletcontextp:: überlappungsmethode

Verschiebt einen Tablet-Kontext an die Vorder-oder Rückseite der Eingabe Warteschlange.

## <a name="syntax"></a>Syntax


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*btop* \[ in\]
</dt> <dd>

Gibt an, ob der Tablet-Kontext an den oberen oder unteren Rand der Eingabe Warteschlange verschoben werden soll.

</dd> <dt>

*pdwtcid* \[ vorgenommen\]
</dt> <dd>

Der Tablet-Kontext Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletcontextp-Schnittstelle**](itabletcontextp.md)
</dt> </dl>

 

 




