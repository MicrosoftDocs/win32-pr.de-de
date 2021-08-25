---
description: 'IEnumTime::Next-Methode: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: IEnumTime::Next-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6068d23fae96d5623ced72f44e6e8d185f861b6c49ff085f1b6e9e58bc489b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905960"
---
# <a name="ienumtimenext-method"></a>IEnumTime::Next-Methode

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Next-Methode** ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.

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

*Celt* \[ In\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf die [**ITTime-Schnittstelle.**](ittime.md)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann **NULL** sein, wenn *Celt* 1 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode hat die anzahl der *Elemente zurückgegeben.*<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Die Anzahl der verbleibenden Elemente war kleiner als *die von Celt.*<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>       |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die **AddRef-Methode** für die [**ITTime-Schnittstelle**](ittime.md) auf, die von **IEnumTime::Next** zurückgegeben wird. Die Anwendung muss **Release** auf der **ITTime-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




