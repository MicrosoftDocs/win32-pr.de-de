---
description: Die getrecursivelayeroftype-Methode führt eine gründliche Reihenfolge der in dieser Komposition enthaltenen virtuellen Spuren durch und ruft den virtuellen n-ten Titel aus dieser Reihenfolge ab.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Iamtimelinecomp:: getrecursivelayeroftype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362082"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>Iamtimelinecomp:: getrecursivelayeroftype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetRecursiveLayerOfType` -Methode führt eine gründliche Reihenfolge der in dieser Komposition enthaltenen virtuellen Spuren durch und ruft die *n*-te virtuelle Spur aus dieser Reihenfolge ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppvirtualtrack* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des virtuellen Titels.

</dd> <dt>

*Whichlayer* 
</dt> <dd>

Gibt an, welche virtuelle Spur abgerufen werden soll, indiziert von NULL.

</dd> <dt>

*Type* 
</dt> <dd>

Member des Enumerationstyps für den [**\_ \_ Haupttyp der Zeitachse**](timeline-major-type.md) , der angibt, ob die Suche nachverfolgt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                  | Beschreibung                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Kein Objekt vom angegebenen Typ.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

In der Regel ist es nicht erforderlich, dass eine Anwendung diese Methode aufruft.

Wenn es sich bei dem *Typparameter* um einen Zeitachse \_ \_ -Haupttyp \_ Track handelt, umfasst die Tiefe der ersten Reihenfolge Wenn dies nicht der Fall ist, enthält Sie nur die Komposition und Gruppen. Das Objekt selbst ist in der Reihenfolge enthalten.

In der folgenden Anordnung, beginnend bei der Komposition A, wäre die Reihenfolge z. B. B, C, F, D, E, a.

![getrecursivelayeroftype](images/composition.png)

Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

[**Iamtimelinecomp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




