---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Ienumteilnehmer:: Next-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364471"
---
# <a name="ienumparticipantnext-method"></a>Ienumteilnehmer:: Next-Methode

\[**Als nächstes** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Next** -Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*ppelements* \[ vorgenommen\]
</dt> <dd>

Zeiger auf [**itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) -Schnittstellen.

</dd> <dt>

*pceltfetch* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann **null** sein, wenn es sich um einen *celt* handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Von der Methode wurde *die Anzahl der* Elemente zurückgegeben.<br/>           |
| <dl> <dt>**S \_ false**</dt> </dl>       | Die Anzahl der verbleibenden Elemente war kleiner als *celt*.<br/>   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppelements* -Parameter ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode für die [**itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) -Schnittstelle auf, die von **ienumteilnehmer:: Next** zurückgegeben wurde. Die Anwendung muss Release auf der **itagenthandler** -Schnittstelle aufzurufen, um Ressourcen frei [**zugeben**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumteilnehmer**](ienumparticipant.md)
</dt> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> </dl>

 

