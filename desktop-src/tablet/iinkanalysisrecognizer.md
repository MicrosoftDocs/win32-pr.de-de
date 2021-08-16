---
description: Ermöglicht den Zugriff auf Handschrifterkennungen für die Verwendung mit der Ink-Analyse.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: IInkAnalysisRecognizer-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d0736288658c57c1cfd346b8337f91353638b8326ed1d0b29687c812db72efba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350880"
---
# <a name="iinkanalysisrecognizer-interface"></a>IInkAnalysisRecognizer-Schnittstelle

Ermöglicht den Zugriff auf Handschrifterkennungen für die Verwendung mit der Ink-Analyse.

## <a name="members"></a>Member

Die **IInkAnalysisRecognizer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalysisRecognizer** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IInkAnalysisRecognizer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Ruft die Funktionen der -Erkennen ab.<br/>                                                                       |
| [**Getguid**](iinkanalysisrecognizer-getguid.md)                               | Ruft den GUID (Globally Unique Identifier) der Erkennung ab.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Ruft die Bezeichner für die Von **IInkAnalysisRecognizer** unterstützten Locales ab.<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Ruft den Namen der Erkannten ab.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Ruft die GUIDs (Globally Unique Identifiers) für die Eigenschaften ab, die von **diesem IInkAnalysisRecognizer unterstützt** werden.<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | Ruft den Herstellernamen von **IInkAnalysisRecognizer ab.**<br/>                                                        |



 

## <a name="remarks"></a>Hinweise

Eine Erkennung verfügt über bestimmte Attribute und Eigenschaften, die die Erkennung ermöglichen. Die Eigenschaften einer Erkennung müssen bestimmt werden, bevor die Erkennung erfolgen kann. Die Typen von Eigenschaften, die von einer Erkennung unterstützt werden, bestimmen die Erkennungstypen, die sie ausführen kann. Wenn beispielsweise eine Recognizer-Funktion keine cursive Handschrift unterstützt, gibt sie ungenaue Ergebnisse zurück, wenn ein Benutzer in cursive schreibt.

Eine Recognizer-Funktion verfügt auch über integrierte Funktionen, mit denen viele Aspekte der Handschrift automatisch verwaltet werden. Beispielsweise werden die Metriken für die Linien bestimmt, auf denen Striche gezeichnet werden. Sie können die Zeilennummer eines Strichs zurückgeben, aber Sie müssen nie angeben, wie diese Zeilenmetriken aufgrund der integrierten Funktionen der -Wiedererkennung bestimmt werden.

Der [**IInkAnalyzer**](iinkanalyzer.md) verwaltet eine Liste der verfügbaren Recognizer. Verwenden Sie für den Zugriff auf diese Liste die [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode.**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Kontextknotentypen](context-node-types.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

