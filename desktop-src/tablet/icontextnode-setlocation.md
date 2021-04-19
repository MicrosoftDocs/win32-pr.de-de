---
description: Aktualisiert den Bereich dieses icontextnode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'Icontextnode:: setLocation-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356778"
---
# <a name="icontextnodesetlocation-method"></a>Icontextnode:: setLocation-Methode

Aktualisiert den Bereich dieses [**icontextnode**](icontextnode.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pianalysisregion* \[ in\]
</dt> <dd>

Der [**ianalysisregion**](ianalysisregion.md) , der den Bereich beschreibt, in den der Speicherort des [**icontextnode**](icontextnode.md) -Objekts festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um den Speicherort des Kontext Knotens zu aktualisieren (siehe [**icontextnode:: getLocation**](icontextnode-getlocation.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Icontextnode:: getLocation**](icontextnode-getlocation.md)
</dt> <dt>

[**Icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




