---
description: Ruft eine eindeutige Sitzungs-ID ab, die für diese Sitzung erstellt wurde.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'IMF mediakeysession:: get_SessionId-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106369929"
---
# <a name="imfmediakeysessionget_sessionid-method"></a>IMF mediakeysession:: get \_ SessionID-Methode

Ruft eine eindeutige Sitzungs-ID ab, die für diese Sitzung erstellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sessionId* 
</dt> <dd>

Die ID der Medien schlüsselsitzung.

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

[**IMF mediakeysession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




