---
title: IAMWMBufferPassCallback Notify-Methode
description: Die Notify-Methode wird vom Pin für jeden Puffer aufgerufen, der während des Streamings übermittelt wird.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Benachrichtigen von Methodenfenstern im Medienformat
- Notify method windows Media Format , IAMWMBufferPassCallback interface
- IAMWMBufferPassCallback-Schnittstelle windows Media Format , Notify-Methode
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847535"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>IAMWMBufferPassCallback::Notify-Methode

Die **Notify-Methode** wird vom Pin für jeden Puffer aufgerufen, der während des Streamings übermittelt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNSSBuffer3* \[ In\]
</dt> <dd>

Zeiger auf die [**INSSBuffer3-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) die im Medienbeispiel verfügbar gemacht wird.

</dd> <dt>

*pPin* \[ In\]
</dt> <dd>

Zeiger auf den Pin, der dem Medienstream zugeordnet ist, zu dem das Beispiel gehört.

</dd> <dt>

*prtStart* \[ In\]
</dt> <dd>

Startzeit des Beispiels.

</dd> <dt>

*prtEnd* \[ In\]
</dt> <dd>

Endzeit des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es wird kein bestimmter Rückgabewert angegeben. Der aufrufende Pin ignoriert das **HRESULT**.

## <a name="remarks"></a>Hinweise

Mit dieser Methode kann eine Anwendung Informationen im Medienpuffer untersuchen und darauf reagieren, bevor der Pufferinhalt verarbeitet wird. Die Anwendung ist dafür verantwortlich, den Medientyp auf dem Pin zu kennen. Diese Informationen können abgerufen werden, indem zuerst die Streaminformationen aus dem Profil abgerufen und dann die [**IConfigAsfWriter2::StreamNumFromPin-Methode**](iconfigasfwriter2-streamnumfrompin.md) aufgerufen wird, um zu bestimmen, welcher Pin den einzelnen Datenströmen zugeordnet ist.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DirectShow-QASF-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**IAMWMBufferPassCallback-Schnittstelle**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**INSSBuffer3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 