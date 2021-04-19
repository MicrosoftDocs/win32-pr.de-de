---
description: Ruft einen Wert ab, der angibt, ob der angegebene MIME-Typ von der Medienquelle unterstützt wird.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Imfmediasourceextension:: istypesupportiert-Methode'
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
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366553"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>Imfmediasourceextension:: istypesupportiert-Methode

Ruft einen Wert ab, der angibt, ob der angegebene MIME-Typ von der Medienquelle unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Der Medientyp, für den Unterstützung überprüft werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**true** , wenn der Medientyp unterstützt wird. andernfalls **false**.

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

 

 




