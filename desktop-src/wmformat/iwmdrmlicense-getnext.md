---
title: IWMDRMLicense GetNext-Methode (Wmdrmsdk.h)
description: Die GetNext-Methode lädt die Informationen zum nächsten Element in der Liste.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- GetNext-Methode windows Media Format
- GetNext-Methode windows Media Format , IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , GetNext-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0905bc695d1317cc7e4a6a1933292ad68afa8f3e3aadb9572e7a7185f4089c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847137"
---
# <a name="iwmdrmlicensegetnext-method"></a>IWMDRMLicense::GetNext-Methode

Die **GetNext-Methode** lädt die Informationen zum nächsten Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ \_ DRM- WIES ZU \_ \_ KLEIN**</dt> </dl> | Eine aktualisierte Inhaltssperrliste ist erforderlich.<br/> |
| <dl> <dt>**FEHLER: \_ KEINE \_ WEITEREN \_ ELEMENTE**</dt> </dl>      | In der Liste sind keine Elemente mehr vorhanden.<br/>          |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Die Methoden der [**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md) stellen Daten zu einer einzelnen Lizenz gleichzeitig bereit. Das zugrunde liegende -Objekt enthält eine Liste mit einer oder mehreren Lizenzen. Wenn Sie diese Methode aufrufen, verschiebt die Schnittstelle ihre internen Verweise auf die nächste Lizenz in der Liste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





