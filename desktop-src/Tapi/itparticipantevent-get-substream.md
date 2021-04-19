---
description: Der get- \_ substream erhält einen Zeiger auf ein Array von itsubstream-Schnittstellen, die die am Ereignis beteiligten untergeordneten Datenströme darstellen.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Itparticipvorgänger Vent:: get_SubStream-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372088"
---
# <a name="itparticipanteventget_substream-method"></a>Itparticipvorgänger Vent:: get \_ substream-Methode

\[**get \_ Substream** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Der **get- \_ substream** erhält einen Zeiger auf ein Array von [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstellen, die die am Ereignis beteiligten untergeordneten Datenströme darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsubstream* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Zeigern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                           | Bedeutung                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ noItems**</dt> </dl> | Dem Ereignis sind keine Substreams zugeordnet.<br/>   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>   | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>       | Der *ppsubstream* -Parameter ist kein gültiger Zeiger.<br/>  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itparticipvorgänger Vent**](itparticipantevent.md)
</dt> <dt>

[**Itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

