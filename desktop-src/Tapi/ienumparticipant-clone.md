---
description: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'Ienumparticipants:: Clone-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371339"
---
# <a name="ienumparticipantclone-method"></a>Ienumteilnehmer:: Clone-Methode

\[**Clone** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Clone** -Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die neue [**ienumteilnehmer**](ienumparticipant.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der *ppum* -Parameter ist kein gültiger Zeiger.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>  | Aus unbekannten Gründen fehlgeschlagen.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

TAPI Ruft die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode für die [**ienumparticipants**](ienumparticipant.md) -Schnittstelle auf, die von **ienumteilnehmer:: Clone** zurückgegeben wurde. Die Anwendung muss Release auf der **ienumparticipants** -Schnittstelle aufzurufen, um Ihnen zugeordnete Ressourcen frei [**zugeben**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .

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

 

