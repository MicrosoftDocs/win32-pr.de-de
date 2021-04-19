---
title: Iwmdrmeventgenerator cancelasyncoperation-Methode (wmdrmsdk. h)
description: Die cancelasyncoperation-Methode bricht einen asynchronen Vorgang ab.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Cancelasyncoperation-Methode, Windows Media-Format
- Cancelasyncoperation-Methode, Windows Media-Format, iwmdrmeventgenerator-Schnittstelle
- Iwmdrmeventgenerator-Schnittstelle Windows Media-Format, cancelasyncoperation-Methode
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
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367044"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>Iwmdrmeventgenerator:: cancelasyncoperation-Methode

Die **cancelasyncoperation** -Methode bricht einen asynchronen Vorgang ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*punkcancelationcookie* \[ in\]
</dt> <dd>

Zeiger auf das Abbruch Cookie, das den asynchronen Vorgang identifiziert, der abgebrochen werden soll. Dieses Cookie wird von der-Methode bereitgestellt, mit der der Vorgang gestartet wird.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmeventgenerator-Schnittstelle**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





