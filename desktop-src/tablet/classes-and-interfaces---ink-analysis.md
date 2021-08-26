---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die bei der Ink-Analyse verwendet werden. Die Klassen und Schnittstellen für die Ink-Analyse sind nicht automation-kompatibel.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Klassen und Schnittstellen für die Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48335b0e7bf6e29ee90cf1dbf8fb3e96fd761c4b8c0194daaa9d7365fe89d5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937020"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Klassen und Schnittstellen für die Ink-Analyse

Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die bei der Ink-Analyse verwendet werden. Die Klassen und Schnittstellen für die Ink-Analyse sind nicht automation-kompatibel.

## <a name="classes"></a>Klassen



| Klasse                                    | Beschreibung                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**Analysisregion**](analysisregion.md) | Implementiert die [**IAnalysisRegion-Schnittstelle.**](ianalysisregion.md)<br/> |
| [**Inkanalyzer**](inkanalyzer.md)       | Implementiert die [**IInkAnalyzer-Schnittstelle.**](iinkanalyzer.md)<br/>       |



 

## <a name="interfaces"></a>Schnittstellen



| Schnittstelle                                                    | BESCHREIBUNG                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Stellt die möglichen Übereinstimmungen von Handschrifterkennungsworten für [**IContextNode-Objekte**](icontextnode.md) dar.<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Enthält eine Auflistung von -Objekten, die die [**IAnalysisAlternate-Schnittstelle**](ianalysisalternate.md) implementieren und das Ergebnis der Ink-Analyse sind.<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Stellt den Status des Ink-Analyse-Vorgangs dar, indem beschrieben wird, ob die Analyse erfolgreich abgeschlossen wurde und ob Warnungen aufgetreten sind.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Stellt eine Warnung oder einen Fehler dar, die während eines Ink-Analyse-Vorgangs auftritt.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Enthält eine Auflistung von -Objekten, die die [**IAnalysisWarning-Schnittstelle**](ianalysiswarning.md) implementieren und das Ergebnis eines Ink-Analyse-Vorgangs sind.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Stellt eine Beziehung zwischen zwei [**IContextNode-Objekten**](icontextnode.md) dar.<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Enthält eine Auflistung von -Objekten, die die [**IContextLink-Schnittstelle**](icontextlink.md) implementieren.<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Stellt einen Knoten in einer Struktur von -Objekten dar, die im Rahmen der Ink-Analyse erstellt werden.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Enthält eine Auflistung von -Objekten, die die [**IContextNode-Schnittstelle**](icontextnode.md) implementieren und das Ergebnis eines Ink-Analyse-Vorgangs sind.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Ermöglicht den Zugriff auf Handschrifterkennungen für die Verwendung mit der Ink-Analyse.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Enthält eine Auflistung von -Objekten, die die [**IInkAnalysisRecognizer-Schnittstelle**](iinkanalysisrecognizer.md) implementieren und die Fähigkeit zum Erkennen von Handschrift, Objekten oder Gesten darstellen.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Bietet Zugriff auf Layoutanalyse, Schreib- und Zeichnungklassifizierung und Handschrifterkennung.<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Macht eine Methode verfügbar, um zu bewerten, ob ein [**IContextNode-Objekt**](icontextnode.md) ein angegebenes Kriterium erfüllt oder fehlschlägt.<br/>                                                                              |



 

## <a name="return-values"></a>Rückgabewerte

Methoden in der Tablet PC-COM-Bibliothek geben Werte von **HRESULT zurück.** Sofern nicht anders angegeben, werden die Bedeutungen der **HRESULT-Werte** in dieser Tabelle beschrieben.



| HRESULT-Wert                                   | Beschreibung                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Erfolg.<br/>                                                                      |
| \_E-ZEIGER<br/>                           | Mindestens ein Zeiger (für einen Eingabe- oder einen Ausgabeparameter) ist ungültig.<br/> |
| E \_ INVALIDARG<br/>                        | Member hat versucht, ein ungültiges Argument zu übergeben.<br/>                              |
| \_E-INK-AUSNAHME \_<br/>                    | Ausnahme.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | Das System kann keinen Arbeitsspeicher zuordnen, um den Vorgang abschließen zu können.<br/>                      |
| E \_ FAIL<br/>                              | Nicht angegebener Fehler.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | Member hat versucht, einen ungültigen Vorgang zu verwenden.<br/>                                 |
| TPC \_ E \_ UNGÜLTIGER \_ MODUS<br/>                | Member hat versucht, einen ungültigen Modus zu verwenden.<br/>                                      |
| TPC \_ E \_ UNGÜLTIGE \_ KONFIGURATION<br/>       | Der Member hat versucht, eine ungültige Konfiguration zu verwenden.<br/>                             |
| TPC \_ E \_ UNGÜLTIGE \_ \_ PAKETBESCHREIBUNG<br/> | Member hat versucht, eine ungültige Paketbeschreibung zu verwenden.<br/>                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




