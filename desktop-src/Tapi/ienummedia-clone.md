---
description: 'IEnumMedia::Clone-Methode: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: IEnumMedia::Clone-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114548"
---
# <a name="ienummediaclone-method"></a>IEnumMedia::Clone-Methode

\[ Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Clone-Methode** erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Zeiger auf das neue [**IEnumMedia-Objekt.**](ienummedia.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppEnum-Parameter* ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Fehler aus unbekannten Gründen.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

TAPI ruft die **AddRef-Methode** für die [**IEnumMedia-Schnittstelle**](ienummedia.md) auf, die von **IEnumMedia::Clone** zurückgegeben wird. Die Anwendung muss **Release** auf der **IEnumMedia-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

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

 

 




