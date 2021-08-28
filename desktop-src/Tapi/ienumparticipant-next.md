---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab. Diese Methode ist vor Visual Basic und Skriptsprachen verborgen.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: IEnumParticipant::Next-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d574f7c34bc48679ea679caf8ba07c881bcd1c692fa3215ae48a9ecf54d7cbfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003588"
---
# <a name="ienumparticipantnext-method"></a>IEnumParticipant::Next-Methode

\[**Next** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Next-Methode** ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab. Diese Methode ist vor Visual Basic und Skriptsprachen verborgen.

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

*celt* \[ In\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*ppElements* \[ out\]
</dt> <dd>

Zeiger auf [**ITAgentHandler-Schnittstellen.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann **NULL** sein, wenn *Celt* eins ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode hat die anzahl der *Elemente zurückgegeben.*<br/>           |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Die Anzahl der verbleibenden Elemente war kleiner als *die von Celt.*<br/>   |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppElements-Parameter* ist kein gültiger Zeiger.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die [**AddRef-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für die [**ITAgentHandler-Schnittstelle**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) auf, die von **IEnumParticipant::Next** zurückgegeben wird. Die Anwendung muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf der **ITAgentHandler-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

