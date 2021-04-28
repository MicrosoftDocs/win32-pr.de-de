---
description: 'IEnumTime::Next-Methode: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: IEnumTime::Next-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118388"
---
# <a name="ienumtimenext-method"></a>IEnumTime::Next-Methode

\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

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

*celt* \[ In\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf die [**ITTime-Schnittstelle.**](ittime.md)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann NULL **sein,** *wenn celt* gleich 1 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode hat *die Anzahl der* Elemente zurückgegeben.<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Die Anzahl der verbleibenden Elemente war kleiner *als celt.*<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

TAPI ruft die **AddRef-Methode** für die [**ITTime-Schnittstelle**](ittime.md) auf, die von **IEnumTime::Next** zurückgegeben wird. Die Anwendung muss **Release** auf der **ITTime-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




