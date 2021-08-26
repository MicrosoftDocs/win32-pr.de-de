---
description: Entfernt den angegebenen Quellpuffer aus der Auflistung von Quellpuffern, die durch das -OBJEKT DERMEDIASourceExtension verwaltet werden.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: MÜSSENMediaSourceExtension::RemoveSourceBuffer-Methode
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
ms.openlocfilehash: 52c15882b57191169f033ab8a3b6c2f50f10f8e20b8f081c7bc70b7509b9a58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013970"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>MÜSSENMediaSourceExtension::RemoveSourceBuffer-Methode

Entfernt den angegebenen Quellpuffer aus der Auflistung von Quellpuffern, die vom [**-OBJEKT DER MEDIENQUELLEQuelleExtension verwaltet**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSourceBuffer* \[ In\]
</dt> <dd>

Der zu entfernende Puffer.

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

[**DURCHSCHN.MediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




