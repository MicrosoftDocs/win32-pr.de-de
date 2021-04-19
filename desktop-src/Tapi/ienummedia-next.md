---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'Ienummedia:: Next-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365814"
---
# <a name="ienummedianext-method"></a>Ienummedia:: Next-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Next** -Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*PVal* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die [**ITmedia**](itmedia.md) -Schnittstelle.

</dd> <dt>

*pceltfetch* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann **null** sein, wenn es sich um einen *celt* handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Von der Methode wurde *die Anzahl der* Elemente zurückgegeben.<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | Die Anzahl der verbleibenden Elemente war kleiner als *celt*.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Der *PVal* -Parameter ist kein gültiger Zeiger.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode auf der [**ITmedia**](itmedia.md) -Schnittstelle auf, die von **ienummedia:: Next** zurückgegeben wurde. Die Anwendung muss Release auf der **ITmedia** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienummedia**](ienummedia.md)
</dt> </dl>

 

 




