---
title: WMDRMShutdown-Funktion (Wmdrmsdk.h)
description: Die WMDRMShutdown-Funktion gibt Ressourcen frei, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- WMDRMShutdown-Funktion windows Media Format
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
ms.openlocfilehash: f80f0f7264cd0962cb642f0877ccd044e777c3e9f269f87fcffc0037dcc0836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930366"
---
# <a name="wmdrmshutdown-function"></a>WMDRMShutdown-Funktion

Die **WMDRMShutdown-Funktion** gibt Ressourcen frei, die von den erweiterten APIs des Windows Media DRM-Clients verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Um Speicherverluste zu vermeiden, müssen Sie diese Funktion für jeden Aufruf der [**WMDRMStartup-Funktion**](wmdrmstartup.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Funktionen**](drm-functions.md)
</dt> </dl>

 

 





