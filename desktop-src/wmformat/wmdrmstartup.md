---
title: Wmdrmstartup-Funktion (wmdrmsdk. h)
description: Die wmdrmstartup-Funktion initialisiert Ressourcen, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Wmdrmstartup-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359691"
---
# <a name="wmdrmstartup-function"></a>Wmdrmstartup-Funktion

Die **wmdrmstartup** -Funktion initialisiert Ressourcen, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Für jeden Aufrufe dieser Funktion müssen Sie [**wmdrmshutdown**](wmdrmshutdown.md) anrufen, um die verwendeten Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Funktionen**](drm-functions.md)
</dt> </dl>

 

 





