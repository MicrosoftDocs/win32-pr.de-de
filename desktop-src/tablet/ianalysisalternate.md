---
description: Steht für die möglichen Handschrift Erkennungs Wort Übereinstimmungen für icontextnode-Objekte.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Ianalysisalternate-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214683"
---
# <a name="ianalysisalternate-interface"></a>Ianalysisalternate-Schnittstelle

Steht für die möglichen Handschrift Erkennungs Wort Übereinstimmungen für [**icontextnode**](icontextnode.md) -Objekte.

## <a name="members"></a>Member

Die **ianalysisalternate** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ianalysisalternate** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ianalysisalternate** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getalternatenodes**](ianalysisalternate-getalternatenodes.md)               | Ruft die [**icontextnode**](icontextnode.md) -Objekte ab, die mit dieser alternativen verknüpft sind.<br/>                                                       |
| [**Getrecognitionconfidence**](ianalysisalternate-getrecognitionconfidence.md) | Ruft einen Wert ab, der die Vertrauens Ebene angibt, die der [**iinkanalyzer**](iinkanalyzer.md) in der Genauigkeit von **ianalysisalternate** hat.<br/> |
| [**GetRecognizedString**](ianalysisalternate-getrecognizedstring.md)           | Ruft den erkannten Zeichen folgen Wert des **ianalysisalternate** -Objekts ab.<br/>                                                                               |
| [**GetStrokeIds**](ianalysisalternate-getstrokeids.md)                         | Ruft die Strich Bezeichner ab, die diesem **ianalysisalternate**-Element zugeordnet sind.<br/>                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Es gibt viele Variationen der Benutzer Handschrift. Aus diesem Grund kann die Handschrifterkennung manchmal in Text konvertieren, der sich von dem beabsichtigten Benutzer unterscheidet. Wenn ein [**iinkanalyzer**](iinkanalyzer.md) eine Analyse für eine Auflistung von Strichen durchführt, sucht **iinkanalyzer** nach dem wahrscheinlichsten Satz von Wörtern, den die Handschrift darstellt. Außerdem findet der **iinkanalyzer** auch Sätze alternativer Erkennungs Übereinstimmungen, die in einer [**ianalysisalterors**](ianalysisalternates.md) -Auflistung gespeichert sind. Damit ein Benutzer Erkennungs Alternativen nutzen kann, müssen Sie eine Benutzeroberfläche erstellen, die es dem Benutzer ermöglicht, die richtige **ianalysisalternate** auszuwählen.

**Ianalysisalternate** -Objekte werden in der Regel durch die [**iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)abgerufen. Das erste **ianalysisalternate** -Objekt in der Auflistung ist das, was [**iinkanalyzer**](iinkanalyzer.md) als wahrscheinlichste Alternative ansieht.

Diese Schnittstelle entspricht [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) im .NET Framework.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisalteraten**](ianalysisalternates.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforstrokes-Methode**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

