---
description: Legt das Beispiel für die Medienstrom Quelle fest.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Imfmediastreamsourcesamplerequest:: setSample-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366370"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a>Imfmediastreamsourcesamplerequest:: setSample-Methode

Legt das Beispiel für die Medienstrom Quelle fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Das Beispiel für die Medienstrom Quelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                       |
| IDL<br/>                      | <dl> <dt>MFI. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfmediastreamsourcesamplerequest**](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




