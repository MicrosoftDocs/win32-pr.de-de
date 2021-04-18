---
title: Iwmdrmindividualizationstatus GetStatus-Methode (wmdrmsdk. h)
description: Mit der GetStatus-Methode werden ausführliche Informationen zum Individualisierungs Fortschritt abgerufen.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- GetStatus-Methode Windows Media-Format
- GetStatus-Methode Windows Media-Format, iwmdrmindividualizationstatus-Schnittstelle
- Iwmdrmindividualizationstatus-Schnittstelle Windows Media-Format, GetStatus-Methode
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371130"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>Iwmdrmindividualizationstatus:: GetStatus-Methode

Mit der **GetStatus** -Methode werden ausführliche Informationen zum Individualisierungs Fortschritt abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstatus* \[ vorgenommen\]
</dt> <dd>

Empfängt eine [**WM \_ Individual- \_ Status**](drmwm-individualize-status.md) Struktur, die ausführliche Informationen zum Status des Individualisierungs Versuchs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmindividualizationstatus-Schnittstelle**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





