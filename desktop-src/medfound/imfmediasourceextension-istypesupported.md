---
description: Ruft einen Wert ab, der angibt, ob der angegebene MIME-Typ von der Medienquelle unterstützt wird.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: MÜSSENMediaSourceExtension::IsTypeSupported-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: e2292ab717914e29a7741fed997b0f8b8b16e152e2fa889dd7ecb04bbb98aaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974339"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>MÜSSENMediaSourceExtension::IsTypeSupported-Methode

Ruft einen Wert ab, der angibt, ob der angegebene MIME-Typ von der Medienquelle unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Der Medientyp, auf den die Unterstützung überprüft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn der Medientyp unterstützt wird; andernfalls **FALSE.**

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

 

 




