---
description: Ermöglicht den Zugriff auf Handschrift erkennungsungen für die Verwendung mit der Ink-Analyse.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Iinkanalysiserkenzer-Schnittstelle (iacom. h)
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
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368098"
---
# <a name="iinkanalysisrecognizer-interface"></a>Iinkanalysiserkenzer-Schnittstelle

Ermöglicht den Zugriff auf Handschrift erkennungsungen für die Verwendung mit der Ink-Analyse.

## <a name="members"></a>Member

Die **iinkanalysiserkenzer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iinkanalysiserkenzer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iinkanalysiserkenzer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Ruft die Funktionen des Erkennungs Moduls ab.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Ruft den Globally Unique Identifier (GUID) der Erkennung ab.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Ruft die Bezeichner für die Gebiets Schemas ab, die von diesem **iinkanalysiserkenzer** unterstützt werden.<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Ruft den Namen der Erkennung ab.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Ruft die GUIDs (Global Unique Bezeichner) für die Eigenschaften ab, die von diesem **iinkanalysiserkenzer** unterstützt werden.<br/> |
| [**Getvendor**](iinkanalysisrecognizer-getvendor.md)                           | Ruft den Herstellernamen des **iinkanalysiserkenzer**-Elements ab.<br/>                                                        |



 

## <a name="remarks"></a>Bemerkungen

Eine Erkennung verfügt über bestimmte Attribute und Eigenschaften, mit deren Hilfe Sie eine Erkennung durchführen können. Die Eigenschaften einer Erkennung müssen festgelegt werden, bevor eine Erkennung erfolgen kann. Die Typen von Eigenschaften, die von einer Erkennung unterstützt werden, bestimmen, welche Erkennungs Typen Sie ausführen können. Wenn eine Erkennung beispielsweise keine Kursive Handschrift unterstützt, gibt Sie falsche Ergebnisse zurück, wenn ein Benutzer in einem Cursor schreibt.

Eine Erkennung verfügt auch über eine integrierte Funktionalität, mit der viele Aspekte der Handschrift automatisch verwaltet werden. Beispielsweise bestimmt Sie die Metriken für die Zeilen, in denen Striche gezeichnet werden. Sie können die Zeilennummer eines Strichs zurückgeben. Sie müssen jedoch nie angeben, wie diese Zeilenmetriken aufgrund der integrierten Funktionalität der Erkennung bestimmt werden.

[**Iinkanalyzer**](iinkanalyzer.md) verwaltet eine Liste der verfügbaren erkenzer. Um auf diese Liste zuzugreifen, verwenden Sie die [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methoden**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalysiserkenzers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: kreatecustomerkenzer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

