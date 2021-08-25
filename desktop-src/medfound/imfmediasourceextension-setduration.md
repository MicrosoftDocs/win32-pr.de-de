---
description: Legt die Dauer der Medienquelle in Einheiten von 100 Nanosekunden fest.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: ANDROMediaSourceExtension::SetDuration-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: caad66946514eec91d1cac1dc9745b0d07d1546e32c9548297f01e76b921c46f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061210"
---
# <a name="imfmediasourceextensionsetduration-method"></a>ANDROMediaSourceExtension::SetDuration-Methode

Legt die Dauer der Medienquelle in Einheiten von 100 Nanosekunden fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*duration* \[ In\]
</dt> <dd>

Die Dauer der Medienquelle in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ANDROMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




