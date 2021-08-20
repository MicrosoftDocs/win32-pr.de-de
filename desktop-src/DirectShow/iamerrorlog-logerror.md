---
description: Die LogError-Methode protokolliert einen Fehler. Anwendungen müssen diese Methode nicht aufrufen. Sie wird intern als Reaktion auf Renderingfehler aufgerufen.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: IAMErrorLog::LogError-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d5652bf5fa60fda79a706179d1a8c0e86d91f3eaf6d66c7d3313dba1964846ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999705"
---
# <a name="iamerrorloglogerror-method"></a>IAMErrorLog::LogError-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die **LogError-Methode** protokolliert einen Fehler. Anwendungen müssen diese Methode nicht aufrufen. Sie wird intern als Reaktion auf Renderingfehler aufgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schweregrad* 
</dt> <dd>

Reserviert. Darf nicht verwendet werden.

</dd> <dt>

*ErrorString* 
</dt> <dd>

Zeichenfolgenwert, der den Text des Fehlers enthält.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Fehlercode

</dd> <dt>

*Hresult* 
</dt> <dd>

Der HRESULT-Wert, der vom Methodenaufruf zurückgegeben wurde, der den Fehler verursacht hat.

</dd> <dt>

*pExtraInfo* \[ In\]
</dt> <dd>

Zeiger auf eine VARIANT-Datei, die zusätzliche Informationen zum Fehler enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des *hresult-Parameters* zurück.

## <a name="remarks"></a>Hinweise

Geben Sie in dieser Methode nicht den **VARIANT** frei, auf den *pExtraInfo* zeigt. Außerdem wird der **VARIANT-Wert** ungültig, nachdem die Methode zurückgegeben wurde. Versuchen Sie daher nicht, später darauf zu verweisen.

Implementieren Sie diese Methode, um so schnell wie möglich zurückzugeben. Nehmen Sie innerhalb dieser Methode keine Funktionsaufrufe vor, die die Programmausführung blockieren könnten. Rufen Sie beispielsweise keine Funktionen auf, die Fenstermeldungen senden, Ereignisse blockieren oder anderweitig die Ausführung blockieren. Dies kann dazu führen, dass der Computer nicht mehr reagiert.

Eine Liste der vom DES definierten Fehler sowie die Bedeutung und den Datentyp der **VARIANT,auf** die *von pExtraInfo* verwiesen wird, finden Sie unter [Renderingfehler.](rendering-errors.md)

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMErrorLog-Schnittstelle**](iamerrorlog.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




