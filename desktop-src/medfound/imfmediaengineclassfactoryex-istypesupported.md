---
description: Ruft einen Wert ab, der angibt, ob das angegebene Schlüsselsystem den angegebenen Medientyp unterstützt.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'IMF mediaengineclassfactoryex:: istypesupportiert-Methode'
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
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354900"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>IMF mediaengineclassfactoryex:: istypesupportiert-Methode

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

Der MIME-Typ, für den Unterstützung überprüft werden soll

</dd> <dt>

*Keysystem* 
</dt> <dd>

Das Schlüsselsystem, für das die Unterstützung überprüft wird.

</dd> <dt>

*isSupported* 
</dt> <dd>

**true** , wenn der Typ von *Keysystem* unterstützt wird. andernfalls **false.**

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

[**IMF mediaengineclassfacrenyex**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




