---
description: Fügt der Auflistung der Puffer, die der imfmediasourceextension zugeordnet sind, einen imfsourcebuffer hinzu.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'Imfmediasourceextension:: addsourcebuffer-Methode'
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
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355713"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a>Imfmediasourceextension:: addsourcebuffer-Methode

Fügt der Auflistung der Puffer, die der [**imfmediasourceextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)zugeordnet sind, einen [**imfsourcebuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) hinzu.

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

*Typ* \[ in\]
</dt> <dd></dd> <dt>

*pnotify* \[ in\]
</dt> <dd></dd> <dt>

*ppsourcebuffer* \[ vorgenommen\]
</dt> <dd></dd> </dl>

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

 

 




