---
description: Schließt die Media Key-Sitzung und muss aufgerufen werden, bevor die schlüsselsitzung freigegeben wird.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'IMF mediakeysession:: Close-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364280"
---
# <a name="imfmediakeysessionclose-method"></a>IMF mediakeysession:: Close-Methode

Schließt die Media Key-Sitzung und muss aufgerufen werden, bevor die schlüsselsitzung freigegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**IMF mediakeysession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




