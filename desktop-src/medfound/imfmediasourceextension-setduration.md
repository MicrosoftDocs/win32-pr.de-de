---
description: Legt die Dauer der Medienquelle in 100-Nanosecond-Einheiten fest.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Imfmediasourceextension:: setduration-Methode'
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
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365232"
---
# <a name="imfmediasourceextensionsetduration-method"></a>Imfmediasourceextension:: setduration-Methode

Legt die Dauer der Medienquelle in 100-Nanosecond-Einheiten fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dauer* \[ in\]
</dt> <dd>

Die Dauer der Medienquelle in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfmediasourceextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




