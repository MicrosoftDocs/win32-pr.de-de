---
description: Ruft eine eindeutige Sitzungs-ID ab, die für diese Sitzung erstellt wurde.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: METHODE FÜR DIE 1000-get_SessionId KEYKeySession::get_SessionId
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
ms.openlocfilehash: f598cbb1d7122bb8597d5849778a833462b4e6d9de48942fdfabbc95bbc30898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724550"
---
# <a name="imfmediakeysessionget_sessionid-method"></a>EINEMEDIAKeySession::get \_ SessionId-Methode

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

Die Sitzungs-ID des Medienschlüssels.

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

[**DURCHTASTEMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




