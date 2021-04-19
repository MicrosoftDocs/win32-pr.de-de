---
description: Die LogError-Methode protokolliert einen Fehler. Anwendungen müssen diese Methode nicht aufzurufen. Sie wird intern als Reaktion auf Renderingfehler aufgerufen.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Iamerrorlog:: LogError-Methode (qedit. h)'
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
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372329"
---
# <a name="iamerrorloglogerror-method"></a>Iamerrorlog:: LogError-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **LogError** -Methode protokolliert einen Fehler. Anwendungen müssen diese Methode nicht aufzurufen. Sie wird intern als Reaktion auf Renderingfehler aufgerufen.

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

*Severity* 
</dt> <dd>

Reserviert. Darf nicht verwendet werden.

</dd> <dt>

*ErrorString* 
</dt> <dd>

Ein Zeichen folgen Wert, der den Text des Fehlers enthält.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Fehlercode

</dd> <dt>

*HRESULT* 
</dt> <dd>

Der HRESULT-Wert, der vom Methoden Aufrufwert zurückgegeben wurde, der den Fehler verursacht hat.

</dd> <dt>

*pextrainfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Variante, die alle zusätzlichen Informationen über den Fehler enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des *HRESULT* -Parameters zurück.

## <a name="remarks"></a>Bemerkungen

Freigeben Sie in dieser Methode nicht die **Variante** , auf die *pextrainfo* zeigt. Außerdem wird die **Variante** nach der Rückgabe der Methode ungültig. versuchen Sie später nicht, darauf zu verweisen.

Implementieren Sie diese Methode, um so schnell wie möglich zurückzukehren. Erstellen Sie innerhalb dieser Methode keine Funktionsaufrufe, die möglicherweise die Programmausführung blockieren. Sie können z. b. keine Funktionen aufzurufen, die Fenster Meldungen senden, Ereignisse blockieren oder anderweitig die Ausführung blockieren. Dies könnte dazu führen, dass der Computer nicht mehr reagiert.

Eine Liste der Fehler, die von des definiert werden, sowie die Bedeutung und den Datentyp der **Variant** , auf die *pextrainfo* zeigt, finden Sie unter [Rendern von Fehlern](rendering-errors.md).

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamerrorlog-Schnittstelle**](iamerrorlog.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




