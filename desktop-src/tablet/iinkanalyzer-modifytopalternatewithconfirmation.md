---
description: Ändert die aktuelle obere Alternative in den angegebenen ianalysisalternate.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343689"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode

Ändert die aktuelle obere Alternative in den angegebenen [**ianalysisalternate**](ianalysisalternate.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Alternative* \[ in\]
</dt> <dd>

Die Alternative zur Analyse, die als neue obere Alternative festgelegt werden soll.

</dd> <dt>

*Bestätigung automatisch* \[ in\]
</dt> <dd>

**Variant \_ TRUE** , um alle frei Hand Blatt Kontext-Knoten, die der Analyse entsprechen, auf den Bestätigungs Typ **ConfirmationType \_ NodeTypeAndProperties** festzulegen (siehe [**icontextnode:: isconfirmed**](icontextnode-isconfirmed.md) und [**ConfirmationType**](confirmationtype.md)); **Variant \_ "False** ", um alle frei Hand Blatt Kontext Knoten festzulegen, die der Analyse entsprechen, in den Bestätigungs Typ " **ConfirmationType \_ None**".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Um Analyse Alternativen zu erhalten, verwenden Sie die [**iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md), die [**iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)oder die [**iinkanalyzer:: getalternatesforstriche-Methode**](iinkanalyzer-getalternatesforstrokes.md). Verwenden Sie die [**ianalysisalternate:: getalternatenodes-Methode**](ianalysisalternate-getalternatenodes.md), um die einem alternativen Analyse zugeordneten Kontext Knoten Objekte zu erhalten.

Verwenden Sie [**icontextnode:: Confirm**](icontextnode-confirm.md), um den bestätentyp für einen Kontext Knoten zu ändern.

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

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Bestätigungs Analyse ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Verweis](ink-analysis-reference.md)
</dt> </dl>

 

 




