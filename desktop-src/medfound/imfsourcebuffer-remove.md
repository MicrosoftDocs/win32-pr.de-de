---
description: Entfernt die durch den angegebenen Zeitbereich definierten Mediensegmente aus DEM SOURCESourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: DIE METHODE "WFSourceBuffer::Remove"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: af9aed011a1a4b53733d70646fc14b21e7c97f9d193a60e679f5f5f532679e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941910"
---
# <a name="imfsourcebufferremove-method"></a>DIE METHODE "WFSourceBuffer::Remove"

Entfernt die durch den angegebenen Zeitbereich definierten Mediensegmente aus DEM [**AUSSCHNITTSOURCEBuffer.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)

## <a name="syntax"></a>Syntax


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*starten* \[ In\]
</dt> <dd>

Der Anfang des Zeitbereichs.

</dd> <dt>

*ende* \[ In\]
</dt> <dd>

Das Ende des Zeitbereichs.

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

[**DIE QUELLESOURCEBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




