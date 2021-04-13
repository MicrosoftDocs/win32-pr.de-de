---
title: Wmkreatestreamforurl-Funktion
description: Die wmkreatestreamforurl-Funktion wird von der Anwendung implementiert, um ein COM-IStream-Objekt für eine bestimmte URL zu erstellen.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Wmkreatestreamforurl-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389210"
---
# <a name="wmcreatestreamforurl-function"></a>Wmkreatestreamforurl-Funktion

Die **wmkreatestreamforurl** -Funktion wird von der Anwendung implementiert, um ein com- **IStream** -Objekt für eine bestimmte URL zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszurl* \[ in\]
</dt> <dd>

Zeiger auf eine breit Zeichen-Zeichenfolge, die die URL enthält.

</dd> <dt>

*pfcorrectsource* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Flag, "true" verhindert, dass das SDK andere Quell-Plug-Ins für diese URL ausprobiert.

</dd> <dt>

*PPStream* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Zeiger auf das **IStream** -Objekt, das von der-Methode erstellt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, muss Sie S OK zurückgeben \_ . Wenn dies nicht möglich ist, muss ein entsprechender **HRESULT** -Fehlercode zurückgegeben werden, und \* *PPStream* sollte auf **null** festgelegt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Quell-Plug-ins**](source-plug-ins.md)
</dt> </dl>

 

 




