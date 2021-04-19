---
title: Gettsaudioendpointenreeratorforsession-Rückruffunktion
description: Gibt einen Verweis auf einen audioendpunktenumerator für die angegebene Sitzungs-ID zurück.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Gettsaudioendpointenreeratorforsession-Rückruffunktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346334"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Gettsaudioendpointenreeratorforsession-Rückruffunktion

Gibt einen Verweis auf einen audioendpunktenumerator für die angegebene Sitzungs-ID zurück. Consumer dieses audioendpunktenumerators, z. b. MMDevAPI.dll, rufen diese Funktion auf, um einen audioendpunktenumerator in einer Remotedesktopdienste Sitzung abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SessionID* \[ in\]
</dt> <dd>

Der Bezeichner der Remotedesktopdienste Sitzung.

</dd> <dt>

*ppendpointenreerator* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Zeigers auf eine [**immdeviceenumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in einer Header Datei definiert. Sie sollten diese Funktion in den benutzerdefinierten Endpunkt Enumerator implementieren und exportieren und die im Syntax Block weiter oben in diesem Thema gezeigte Signatur verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Implementieren eines benutzerdefinierten audioendpunkt-Enumerators](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**Immdeviceenumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

