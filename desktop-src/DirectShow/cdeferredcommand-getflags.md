---
description: Die GetFlags-Methode ruft die Kontextflags ab, die dem verzögerten Befehl zugeordnet sind.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: CDeferredCommand.GetFlags-Methode (Ctlutil.h)
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
ms.openlocfilehash: 9c3ee5826c1b4ff81f90c86a6db4517aafc41313e53672486c41ab4847e82674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910190"
---
# <a name="cdeferredcommandgetflags-method"></a>CDeferredCommand.GetFlags-Methode

Die `GetFlags` -Methode ruft die Kontextflags ab, die dem verzögerten Befehl zugeordnet sind.

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
| <dl> <dt>**\_DISPATCH-METHODE**</dt> </dl>         | Führen Sie den Member als Methode aus. Wenn eine Eigenschaft denselben Namen hat, können sowohl dieses als auch das DISPATCH \_ PROPERTYGET-Flag festgelegt werden.<br/>                                               |
| <dl> <dt>**\_DISPATCH-EIGENSCHAFTGET**</dt> </dl>    | Der Member wird als Eigenschaft oder Datenmitglied abgerufen.<br/>                                                                                                         |
| <dl> <dt>**DISPATCH \_ PROPERTYPUT**</dt> </dl>    | Der Member wird als Eigenschaft oder Datenmitglied geändert.<br/>                                                                                                           |
| <dl> <dt>**DISPATCH \_ PROPERTYPUTREF**</dt> </dl> | Der Member wird nicht über eine Wertzuweisung, sondern über eine Verweiszuweisung geändert. Dieses Flag ist nur gültig, wenn die -Eigenschaft einen Verweis auf ein -Objekt akzeptiert.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




