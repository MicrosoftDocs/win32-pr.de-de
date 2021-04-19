---
description: Die GetFlags-Methode ruft die dem verzögerten Befehl zugeordneten kontextflags ab.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Cdeferredcommand. GetFlags-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367205"
---
# <a name="cdeferredcommandgetflags-method"></a>Cdeferredcommand. GetFlags-Methode

Die- `GetFlags` Methode ruft die dem verzögerten Befehl zugeordneten kontexflags ab.

## <a name="syntax"></a>Syntax


```C++
short GetFlags();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück:



| Rückgabecode                                                                                             | Beschreibung                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Dispatch- \_ Methode**</dt> </dl>         | Führen Sie den Member als Methode aus. Wenn eine Eigenschaft denselben Namen hat, können sowohl dieses als auch das Dispatch \_ PropertyGet-Flag festgelegt werden.<br/>                                               |
| <dl> <dt>**Dispatch- \_ PropertyGet**</dt> </dl>    | Der Member wird als Eigenschaft oder Datenmember abgerufen.<br/>                                                                                                         |
| <dl> <dt>**Dispatch- \_ PropertyPut**</dt> </dl>    | Der Member wird als Eigenschaft oder Datenmember geändert.<br/>                                                                                                           |
| <dl> <dt>**Dispatch \_ propertyputref**</dt> </dl> | Der Member wird über eine Verweis Zuweisung und nicht über eine Wert Zuweisung geändert. Dieses Flag ist nur gültig, wenn die-Eigenschaft einen Verweis auf ein-Objekt akzeptiert.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdeferredcommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




