---
description: Ruft das Medien Schlüsselobjekt ab, das der Medien-Engine zugeordnet ist, oder NULL, wenn kein Medien Schlüsselobjekt vorhanden ist.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'IMF mediaengineeme:: get_Keys-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355726"
---
# <a name="imfmediaengineemeget_keys-method"></a>IMF mediaengineeme:: get \_ Keys-Methode

Ruft das Medien Schlüsselobjekt ab, das der Medien-Engine zugeordnet ist, oder **null** , wenn kein Medien Schlüsselobjekt vorhanden ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*or* 
</dt> <dd>

Das Media Keys-Objekt, das der Medien-Engine zugeordnet ist, oder **null** , wenn kein Medien Schlüsselobjekt vorhanden ist.

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

[**IMF mediaengineeme**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




