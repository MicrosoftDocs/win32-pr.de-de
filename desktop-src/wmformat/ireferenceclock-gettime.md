---
title: IReferenceClock getTime-Methode
description: Die getTime-Methode ruft die aktuelle Verweis Zeit ab.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- GetTime-Methode Windows Media-Format
- GetTime-Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, GetTime-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389344"
---
# <a name="ireferenceclockgettime-method"></a>IReferenceClock:: getTime-Methode

Die **GetTime** -Methode ruft die aktuelle Verweis Zeit ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PTIME* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Uhrzeit in 100-Nanosecond-Einheiten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>              |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Der *PTIME* -Parameter ist **null**.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IReferenceClock-Schnittstelle**](ireferenceclock.md)
</dt> </dl>

 

 





