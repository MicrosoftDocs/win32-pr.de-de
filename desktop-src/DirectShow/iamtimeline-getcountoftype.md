---
description: Die getzählto ftype-Methode ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Elementen enthalten sind.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Iamtimeline:: getzählto ftype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370638"
---
# <a name="iamtimelinegetcountoftype-method"></a>Iamtimeline:: getzählto ftype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetCountOfType` -Methode ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Elementen enthalten sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppieren* 
</dt> <dd>

Index Nummer der Gruppe, für die die Anzahl abgerufen werden soll.

</dd> <dt>

*pVal* 
</dt> <dd>

Empfängt rekursiv die Anzahl von Objekten des angegebenen Typs, die in der Gruppe enthalten sind, und alle zugehörigen virtuellen Spuren.

</dd> <dt>

*pvalwithcomps* 
</dt> <dd>

Empfängt die Anzahl, die in *PVal* zurückgegeben wurde, sowie die Anzahl der durchsuchten Kompositionen, einschließlich dieses.

</dd> <dt>

*Majortype* 
</dt> <dd>

Member des enumerierten Typs der [**Zeitachse \_ \_**](timeline-major-type.md) , der den Typ des zu zählenden Objekts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültige Gruppennummer.<br/>      |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Aufrufen dieser Methode entspricht dem Aufrufen von [**iamtimelinecomp:: getzählype**](iamtimelinecomp-getcountoftype.md) für die angegebene Gruppe. Weitere Informationen finden Sie im Abschnitt "Hinweise" dieser Methode.

In der Regel Ruft eine Anwendung diese Methode nicht auf. Sie wird intern von der Rendering-Engine aufgerufen.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




