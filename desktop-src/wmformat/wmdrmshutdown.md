---
title: Wmdrmshutdown-Funktion (wmdrmsdk. h)
description: Die wmdrmshutdown-Funktion gibt Ressourcen frei, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Wmdrmshutdown-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359227"
---
# <a name="wmdrmshutdown-function"></a>Wmdrmshutdown-Funktion

Die **wmdrmshutdown** -Funktion gibt Ressourcen frei, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um Speicher Verluste zu vermeiden, müssen Sie diese Funktion für jeden Aufrufe der [**wmdrmstartup**](wmdrmstartup.md) -Funktion abrufen.

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

 

 





