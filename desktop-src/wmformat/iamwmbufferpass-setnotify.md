---
title: IAMWMBufferPass SetNotify-Methode
description: Die SetNotify-Methode wird von Anwendungen verwendet, um den WM ASF Writer- oder WM ASF Reader-Filter mit einem Zeiger auf die IAMWMBufferPassCallback-Schnittstelle der Anwendung bereitzustellen.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- SetNotify-Methode windows Media Format
- SetNotify-Methode windows Media Format , IAMWMBufferPass-Schnittstelle
- IAMWMBufferPass-Schnittstelle windows Media Format , SetNotify-Methode
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47e189a2654ed4c760fdfcd6ced5506cc90d5e7cc989a7f79979e6d95b0bbfb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847606"
---
# <a name="iamwmbufferpasssetnotify-method"></a>IAMWMBufferPass::SetNotify-Methode

Die **SetNotify-Methode** wird von Anwendungen verwendet, um den WM ASF Writer- oder [WM ASF Reader-Filter](wm-asf-reader-filter.md) mit einem Zeiger auf die [**IAMWMBufferPassCallback-Schnittstelle**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) der Anwendung bereitzustellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCallback* \[ In\]
</dt> <dd>

Zeiger auf die **IAMWMBufferPassCallback-Schnittstelle** der Anwendung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode auf, bevor Sie das Filterdiagramm in den Ausführungszustand versetzen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMWMBufferPass-Schnittstelle**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 