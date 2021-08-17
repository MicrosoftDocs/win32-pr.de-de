---
description: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält. Diese Methode ist vor Visual Basic und Skriptsprachen verborgen.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: IEnumParticipant::Clone-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccd4bd29442daa01e632ae83510a87eebb06cb72beafc206b04d47c3dd761db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140493"
---
# <a name="ienumparticipantclone-method"></a>IEnumParticipant::Clone-Methode

\[**Klonen** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Clone-Methode** erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält. Diese Methode ist vor Visual Basic und Skriptsprachen verborgen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Zeiger auf die neue [**IEnumParticipant-Schnittstelle.**](ienumparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Der *ppEnum-Parameter* ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Fehler aus unbekannten Gründen.<br/>                          |



 

## <a name="remarks"></a>Hinweise

TAPI ruft die [**AddRef-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) für die [**IEnumParticipant-Schnittstelle**](ienumparticipant.md) auf, die von **IEnumParticipant::Clone** zurückgegeben wird. Die Anwendung muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf der **IEnumParticipant-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.

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

 

