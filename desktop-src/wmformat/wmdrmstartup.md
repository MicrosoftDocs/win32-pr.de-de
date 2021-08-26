---
title: WMDRMStartup-Funktion (Wmdrmsdk.h)
description: Die WMDRMStartup-Funktion initialisiert Ressourcen, die von den erweiterten APIs Windows Media DRM Client verwendet werden.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- WMDRMStartup-Funktion windows Media Format
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
ms.openlocfilehash: 8c194a8c060ad1626fde796510c25c83e3e163dafffe9c17df17a7dcec890be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928741"
---
# <a name="wmdrmstartup-function"></a>WMDRMStartup-Funktion

Die **WMDRMStartup-Funktion** initialisiert Ressourcen, die von den erweiterten APIs Windows Media DRM Client verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Für jeden Aufruf dieser Funktion müssen Sie [**WMDRMShutdown**](wmdrmshutdown.md) aufrufen, um die verwendeten Ressourcen frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Funktionen**](drm-functions.md)
</dt> </dl>

 

 





