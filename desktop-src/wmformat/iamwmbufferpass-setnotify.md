---
title: Iamwmbufferpass-setnotify-Methode
description: Die setnotify-Methode wird von Anwendungen verwendet, um den WM-ASF-oder WM-ASF-Lesefilter mit einem Zeiger auf die iamwmbufferpasscallback-Schnittstelle der Anwendung bereitzustellen.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Setnotify-Methode (Windows Media-Format)
- Setnotify-Methode Windows Media-Format, iamwmbufferpass-Schnittstelle
- Iamwmbufferpass-Schnittstelle Windows Media-Format, setnotify-Methode
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390850"
---
# <a name="iamwmbufferpasssetnotify-method"></a>Iamwmbufferpass:: setnotify-Methode

Die **setnotify** -Methode wird von Anwendungen verwendet, um den WM-ASF-oder [WM-ASF-Lesefilter](wm-asf-reader-filter.md) mit einem Zeiger auf die [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Schnittstelle der Anwendung bereitzustellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCallback* \[ in\]
</dt> <dd>

Zeiger auf die **iamwmbufferpasscallback** -Schnittstelle der Anwendung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode auf, bevor das Filter Diagramm in den Status "Run" versetzt wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamwmbufferpass-Schnittstelle**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 