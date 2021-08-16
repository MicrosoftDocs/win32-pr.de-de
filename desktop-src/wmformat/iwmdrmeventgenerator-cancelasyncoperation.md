---
title: IWMDRMEventGenerator CancelAsyncOperation-Methode (Wmdrmsdk.h)
description: Die CancelAsyncOperation-Methode bricht einen asynchronen Vorgang ab.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- CancelAsyncOperation-Methode windows Media Format
- CancelAsyncOperation-Methode windows Media Format , IWMDRMEventGenerator-Schnittstelle
- IWMDRMEventGenerator-Schnittstelle windows Media Format , CancelAsyncOperation-Methode
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ca44fa141d21caeed1d0f16da65a1db61fe319e2b9424600275563e6c5d52f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847157"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>IWMDRMEventGenerator::CancelAsyncOperation-Methode

Die **CancelAsyncOperation-Methode** bricht einen asynchronen Vorgang ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*kateCancelationCookie* \[ In\]
</dt> <dd>

Zeiger auf das Abbruchcookie, das den asynchronen Vorgang identifiziert, der abgebrochen werden soll. Dieses Cookie wird von der Methode bereitgestellt, die zum Starten des Vorgangs verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMEventGenerator-Schnittstelle**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





