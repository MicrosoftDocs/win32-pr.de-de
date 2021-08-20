---
description: Fügt das angegebene Mediensegment an den APPENDSourceBuffer an.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: APPENDSourceBuffer::Append-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ef0e42f942a7d7e4477f52e152ef0f745f6a12b5812cba1a9bb1b0d95679ae7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062847"
---
# <a name="imfsourcebufferappend-method"></a>APPENDSourceBuffer::Append-Methode

Fügt das angegebene Mediensegment an [**den APPENDSourceBuffer an.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)

## <a name="syntax"></a>Syntax


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ In\]
</dt> <dd>

Die zu anfügenden Mediendaten.

</dd> <dt>

*len* \[ In\]
</dt> <dd>

Die Länge der in *pData gespeicherten Mediendaten.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VERERBungsquelle**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




