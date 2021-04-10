---
title: Iamwmbufferpasscallback-Benachrichtigungs Methode
description: Die Notify-Methode wird von der PIN für jeden Puffer aufgerufen, der beim Streaming zugestellt wird.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Notify-Methode Windows Media-Format
- Notify-Methode Windows Media-Format, iamwmbufferpasscallback-Schnittstelle
- Iamwmbufferpasscallback-Schnittstelle Windows Media-Format, Notify-Methode
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102143"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>Iamwmbufferpasscallback:: Notify-Methode

Die **Notify** -Methode wird von der PIN für jeden Puffer aufgerufen, der beim Streaming zugestellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNSSBuffer3* \[ in\]
</dt> <dd>

Zeiger auf die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle, die für das Medien Beispiel verfügbar gemacht wird

</dd> <dt>

*ppin* \[ in\]
</dt> <dd>

Ein Zeiger auf die PIN, die dem Mediendaten Strom zugeordnet ist, zu dem das Beispiel gehört.

</dd> <dt>

*prtstart* \[ in\]
</dt> <dd>

Die Startzeit des Beispiels.

</dd> <dt>

*prtend* \[ in\]
</dt> <dd>

Endzeit des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es ist kein bestimmter Rückgabewert angegeben. Die aufrufenden Pin ignoriert das **HRESULT**.

## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht es einer Anwendung, Informationen im Medien Puffer zu überprüfen und zu bearbeiten, bevor die Puffer Inhalte verarbeitet werden. Die Anwendung ist dafür verantwortlich, den Medientyp in der PIN zu kennen. Diese Informationen können abgerufen werden, indem zuerst die streaminformationen aus dem Profil abgerufen und anschließend die [**IConfigAsfWriter2:: streamnumfrompin**](iconfigasfwriter2-streamnumfrompin.md) -Methode aufgerufen wird, um zu bestimmen, welche Pin den einzelnen Datenströmen zugeordnet ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DirectShow-qasf-Referenz**](directshow-qasf-reference.md)
</dt> <dt>

[**Iamwmbufferpasscallback-Schnittstelle**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**INSSBuffer3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 