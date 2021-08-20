---
description: Ruft einen Wert ab, der angibt, ob das angegebene Schlüsselsystem den angegebenen Medientyp unterstützt.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: ANDROMediaEngineClassFactoryEx::IsTypeSupported-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 588a7fdc02fb59a9dc156f9f141b210d36e4cef131bf353d6c98d9c055392a28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062999"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>ANDROMediaEngineClassFactoryEx::IsTypeSupported-Methode

Ruft einen Wert ab, der angibt, ob das angegebene Schlüsselsystem den angegebenen Medientyp unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* 
</dt> <dd>

Der MIME-Typ, auf den die Unterstützung überprüft werden soll.

</dd> <dt>

*keySystem* 
</dt> <dd>

Das Schlüsselsystem, für das die Unterstützung überprüft werden soll.

</dd> <dt>

*Issupported* 
</dt> <dd>

**TRUE,** wenn der Typ von *keySystem* unterstützt wird; andernfalls **FALSE.**

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

[**ADRMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




