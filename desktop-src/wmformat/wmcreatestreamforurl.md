---
title: WMCreateStreamForURL-Funktion
description: Die WMCreateStreamForURL-Funktion wird von der Anwendung implementiert, um ein COM IStream-Objekt für eine bestimmte URL zu erstellen.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- WMCreateStreamForURL-Funktion windows Media Format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c32302147eeb814c211a77555ab1c9bb3614eddf3d8001015479461e05d40ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653453"
---
# <a name="wmcreatestreamforurl-function"></a>WMCreateStreamForURL-Funktion

Die **WMCreateStreamForURL-Funktion** wird von der Anwendung implementiert, um ein COM **IStream-Objekt** für eine bestimmte URL zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszURL* \[ In\]
</dt> <dd>

Zeiger auf eine Breitzeichenzeichenfolge, die die URL enthält.

</dd> <dt>

*pfCorrectSource* \[ out\]
</dt> <dd>

Der Zeiger auf ein Flag true verhindert, dass das SDK andere Quell-Plug-Ins für diese URL versucht.

</dd> <dt>

*ppStream* \[ out\]
</dt> <dd>

Zeiger auf einen Zeiger auf das von der -Methode erstellte **IStream-Objekt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, muss sie S \_ OK zurückgeben. Wenn ein Fehler auftritt, muss ein entsprechender **HRESULT-Fehlercode** zurückgegeben werden, und \* *ppStream* sollte auf NULL festgelegt **werden.**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Quell-Plug-Ins**](source-plug-ins.md)
</dt> </dl>

 

 




