---
title: GetTSAudioEndpointEnumeratorForSession-Rückruffunktion
description: Gibt einen Verweis auf einen Audioendpunkt-Enumerator für die angegebene Sitzungs-ID zurück.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- GetTSAudioEndpointEnumeratorForSession-Rückruffunktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f64af1d7e886b418ac87cd360302101a60d746d707652f605a648e9812a5547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059588"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>GetTSAudioEndpointEnumeratorForSession-Rückruffunktion

Gibt einen Verweis auf einen Audioendpunkt-Enumerator für die angegebene Sitzungs-ID zurück. Benutzer dieses Audioendpunkt-Enumerators wie MMDevAPI.dll rufen diese Funktion auf, um einen Audioendpunkt-Enumerator in einer Remotedesktopdienste abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SessionId* \[ In\]
</dt> <dd>

Der Bezeichner der Remotedesktopdienste Sitzung.

</dd> <dt>

*ppEndpointEnumerator* \[ out\]
</dt> <dd>

Die Adresse eines Zeigers auf eine [**IMMDeviceEnumerator-Schnittstelle.**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**

## <a name="remarks"></a>Hinweise

Diese Funktion ist nicht in einer Headerdatei definiert. Sie sollten diese Funktion in Ihren benutzerdefinierten Endpunktenumerator implementieren und exportieren und die Signatur verwenden, die weiter oben in diesem Thema im Syntaxblock gezeigt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Implementieren eines benutzerdefinierten Audioendpunkt-Enumerators](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

