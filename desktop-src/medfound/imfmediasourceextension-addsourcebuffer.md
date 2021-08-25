---
description: Fügt der Auflistung von Puffern, die der NSMMediaSourceExtension zugeordnet sind, einen 1000222111111 hinzu.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: MÜSSENMediaSourceExtension::AddSourceBuffer-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: b49a7c4fb0cb9e45ab0c2823d92ceb6e4076dfcaef4d2e8450f1f3d07f474279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942030"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a>MÜSSENMediaSourceExtension::AddSourceBuffer-Methode

Fügt [**der Auflistung von Puffern,**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) die mit [**dem -OBJEKT VERKNÜPFT sind, einen 50-0-Puffer hinzu.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)

## <a name="syntax"></a>Syntax


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd></dd> <dt>

*pNotify* \[ In\]
</dt> <dd></dd> <dt>

*ppSourceBuffer* \[ out\]
</dt> <dd></dd> </dl>

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

[**DURCHSCHN.MediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




