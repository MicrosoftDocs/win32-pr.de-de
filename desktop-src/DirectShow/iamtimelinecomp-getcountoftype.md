---
description: Die getzählto ftype-Methode ruft die Anzahl der Objekte eines angegebenen Typs, die in dieser Komposition enthalten ist, und alle zugehörigen virtuellen Spuren rekursiv ab.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Iamtimelinecomp:: getzählype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356049"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>Iamtimelinecomp:: getzählype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetCountOfType` -Methode ruft die Anzahl der Objekte eines angegebenen Typs, die in dieser Komposition enthalten ist, und alle zugehörigen virtuellen Spuren rekursiv ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt rekursiv die Anzahl der Objekte des angegebenen Typs, die in dieser Komposition und allen virtuellen Spuren enthalten sind.

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

Gibt " \_ OK" zurück, wenn erfolgreich, andernfalls einen E- \_ Zeiger.

## <a name="remarks"></a>Bemerkungen

In der Regel Ruft eine Anwendung diese Methode nicht auf. Sie wird von der Rendering-Engine aufgerufen.

Wenn Sie die Komposition zählen, ist der in *PVal* zurückgegebene Wert 0 (null), und der in *pvalwithcomps* zurückgegebene Wert ist die Anzahl der Kompositionen. Der Wert von *\* pvalwithcomps* enthält die Komposition, auf der Sie die Methode aufzurufen. Wenn Sie diese Methode z. b. für eine leere Komposition aufzurufen, ist *\* pvalwithcomps* gleich 1.

Gruppen dürfen sich nicht innerhalb von Kompositionen befinden, daher können Sie diese Methode nicht zum zählen von Gruppen verwenden. (Die zurückgegebene Anzahl ist immer 0 (null).) Um Gruppen zu zählen, können Sie die [**iamtimeline:: getgroupcount**](iamtimeline-getgroupcount.md) -Methode aufrufen.

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

 

 




