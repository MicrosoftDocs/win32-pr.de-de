---
description: Enthält eine Auflistung von-Objekten, die die iinkanalysiserkenzer-Schnittstelle implementieren und die die Fähigkeit zum Erkennen von Handschrift, Objekten oder Gesten darstellen.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Iinkanalysiserkenzers-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343718"
---
# <a name="iinkanalysisrecognizers-interface"></a>Iinkanalysiserkenzers-Schnittstelle

Enthält eine Auflistung von-Objekten, die die [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Schnittstelle implementieren und die die Fähigkeit zum Erkennen von Handschrift, Objekten oder Gesten darstellen.

## <a name="members"></a>Member

Die **iinkanalysiserkenzers** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iinkanalysiserkenzers** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iinkanalysiserkenzers** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | Ruft die Anzahl der [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekte in dieser Auflistung ab.<br/> |
| [**Getinkanalysiserkenzer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | Ruft das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element am angegebenen Index ab.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

Die [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methoden**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) Methode von [**iinkanalyzer**](iinkanalyzer.md) gibt eine **iinkanalysiserkenzers** -Sammlung zurück, die die auf dem aktuellen Tablet PC verfügbaren frei Hand erkenungen enthält.

Bei einer Spracherkennung gibt die [**iinkanalysiserkenzer:: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) -Methode ein nicht leeres Array zurück. Bei Gesten Erkennungs Programmen und Objekt erkenzern gibt die **iinkanalysiserkenzer:: GetLanguages** -Methode ein leeres Array zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

