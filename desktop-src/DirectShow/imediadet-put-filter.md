---
description: Die Put \_ Filter-Methode gibt einen Quell Filter an, der vom Medien Detektor verwendet werden soll.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: Imediadet::p ut_Filter-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370679"
---
# <a name="imediadetput_filter-method"></a>Imediadet::p UT- \_ Filter Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_Filter` Methode gibt einen Quell Filter an, der vom Medien Detektor verwendet werden soll.

> [!IMPORTANT]
> Fügen Sie den Quell Filter nicht zu Ihrem eigenen Filter Diagramm hinzu, oder verwenden Sie einen Filter, der bereits in einem Filter Diagramm vorhanden ist. Das Medien Erkennungs Objekt erstellt automatisch ein internes Filter Diagramm, und das Platzieren des Filters in einem anderen Diagramm kann zu unerwarteten Ergebnissen führen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Zeiger auf die **IUnknown** -Schnittstelle des Quell Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                             |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | *NewVal* verweist nicht auf einen Filter.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument.<br/>           |



 

## <a name="remarks"></a>Bemerkungen

Bei den meisten Anwendungen ist es einfacher, die [**\_ Dateiname-Methode imediadet::p UT**](imediadet-put-filename.md) mit dem Namen einer Quelldatei aufzurufen.

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

[**Imediadet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




