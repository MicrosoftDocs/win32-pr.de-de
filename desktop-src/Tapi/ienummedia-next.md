---
description: 'IEnumMedia::Next-Methode: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: IEnumMedia::Next-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113438"
---
# <a name="ienummedianext-method"></a>IEnumMedia::Next-Methode

\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Next-Methode** ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.

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

*celt* \[ In\]
</dt> <dd>

Anzahl der angeforderten Elemente.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Zeiger auf die [**ITMedia-Schnittstelle.**](itmedia.md)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente. Kann NULL **sein,** *wenn celt* eins ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                     | Bedeutung                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode hat *die Anzahl der* Elemente zurückgegeben.<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Die Anzahl der verbleibenden Elemente war kleiner *als celt.*<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Der *pVal-Parameter* ist kein gültiger Zeiger.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

TAPI ruft die **AddRef-Methode** auf der [**ITMedia-Schnittstelle**](itmedia.md) auf, die von **IEnumMedia::Next** zurückgegeben wird. Die Anwendung muss **Release** auf der **ITMedia-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




