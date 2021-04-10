---
description: Ruft den Typ des angegebenen Strichs ab.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Iinkanalyzer:: GetStrokeType-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214659"
---
# <a name="iinkanalyzergetstroketype-method"></a>Iinkanalyzer:: GetStrokeType-Methode

Ruft den Typ des angegebenen Strichs ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Strich Bezeichner.

</dd> <dt>

*pstroketype* \[ vorgenommen\]
</dt> <dd>

Die Klassifizierung des angegebenen Strichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn der Typ des Strichs der [**StrokeType**](stroketype.md) -Wert \_ nicht klassifiziert ist, klassifiziert [**iinkanalyzer**](iinkanalyzer.md) den Strich während der frei Hand Analyse. Andernfalls verwendet **iinkanalyzer** den Typ, der auf dem Strich festgelegt ist.

Der Wert von "Stroke Type" wird von [**iinkanalyzer**](iinkanalyzer.md) nicht als Teil der Ink-Analyse festgelegt. Verwenden Sie die [**iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder die [**iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md), um den strichentyp anzugeben oder zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: SetStrokeType-Methode**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**Iinkanalyzer:: SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




