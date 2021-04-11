---
description: Entfernt den angegebenen Quell Puffer aus der Auflistung der Quell Puffer, die vom imfmediasourceextension-Objekt verwaltet werden.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'Imfmediasourceextension:: removesourcebuffer-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351518"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>Imfmediasourceextension:: removesourcebuffer-Methode

Entfernt den angegebenen Quell Puffer aus der Auflistung der Quell Puffer, die vom [**imfmediasourceextension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) -Objekt verwaltet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psourcebuffer* \[ in\]
</dt> <dd>

Der Puffer, der entfernt werden soll.

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

 

 




