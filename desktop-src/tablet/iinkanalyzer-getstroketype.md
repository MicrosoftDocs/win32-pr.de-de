---
description: Ruft den Typ des angegebenen Strichs ab.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: IInkAnalyzer::GetStrokeType-Methode (IACom.h)
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
ms.openlocfilehash: 71bf3775be1c21e59cf41a51fa5a6140e86e44ac81a2863892c1f252666e0f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092140"
---
# <a name="iinkanalyzergetstroketype-method"></a>IInkAnalyzer::GetStrokeType-Methode

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

*lStrokeId* \[ In\]
</dt> <dd>

Der Strichbezeichner.

</dd> <dt>

*pStrokeType* \[ out\]
</dt> <dd>

Die Klassifizierung des angegebenen Strichs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn der Typ des Strichs der [**StrokeType-Wert StrokeType**](stroketype.md) \_ Unclassified ist, klassifiziert [**IInkAnalyzer**](iinkanalyzer.md) den Strich während der Freihandanalyse. Andernfalls verwendet **IInkAnalyzer** den für den Strich festgelegten Typ.

[**IInkAnalyzer**](iinkanalyzer.md) legt den Strichtypwert nicht als Teil der Freihandanalyse fest. Verwenden Sie zum Angeben oder Ändern des Strichtyps die [**IInkAnalyzer::SetStrokeType-Methode**](iinkanalyzer-setstroketype.md) oder [**die IInkAnalyzer::SetStrokesType-Methode.**](iinkanalyzer-setstrokestype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokeType-Methode**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**IInkAnalyzer::SetStrokesType-Methode**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




