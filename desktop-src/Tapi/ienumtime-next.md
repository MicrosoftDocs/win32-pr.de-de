---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'Ienumtime:: Next-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce3d88bc88e808c35ec64f827fd5925ddfe57f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371378"
---
# <a name="ienumtimenext-method"></a>Ienumtime:: Next-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Next** -Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
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

Zeiger auf die [**ittime**](ittime.md) -Schnittstelle.

</dd> <dt>

*pceltfetch* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann **null** sein, wenn *celt* 1 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Von der Methode wurde *die Anzahl der* Elemente zurückgegeben.<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | Die Anzahl der verbleibenden Elemente war kleiner als *celt*.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Der *PVal* -Parameter ist kein gültiger Zeiger.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die **adressf** -Methode für die [**ittime**](ittime.md) -Schnittstelle auf, die von **ienumtime:: Next** zurückgegeben wurde. Die Anwendung muss Release auf der **ittime** -Schnittstelle aufzurufen, um die damit verbundenen Ressourcen frei **zugeben** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumtime**](ienumtime.md)
</dt> </dl>

 

 




