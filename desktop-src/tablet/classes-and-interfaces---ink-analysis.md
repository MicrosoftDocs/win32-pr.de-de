---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die in der Handschrift Analyse verwendet werden. Die frei Hand Analyse Klassen und-Schnittstellen sind nicht Automatisierungs kompatibel.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Freihand-Analyse Klassen und Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524935"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Freihand-Analyse Klassen und Schnittstellen

Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die in der Handschrift Analyse verwendet werden. Die frei Hand Analyse Klassen und-Schnittstellen sind nicht Automatisierungs kompatibel.

## <a name="classes"></a>Klassen



| Klasse                                    | BESCHREIBUNG                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | Implementiert die [**ianalysisregion**](ianalysisregion.md) -Schnittstelle.<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | Implementiert die [**iinkanalyzer**](iinkanalyzer.md) -Schnittstelle.<br/>       |



 

## <a name="interfaces"></a>Schnittstellen



| Schnittstelle                                                    | BESCHREIBUNG                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ianalysisalternate**](ianalysisalternate.md)             | Steht für die möglichen Handschrift Erkennungs Wort Übereinstimmungen für [**icontextnode**](icontextnode.md) -Objekte.<br/>                                                                                        |
| [**Ianalysisalteraten**](ianalysisalternates.md)           | Enthält eine Auflistung von-Objekten, die die [**ianalysisalternate**](ianalysisalternate.md) -Schnittstelle implementieren und die das Ergebnis der frei Hand Analyse sind.<br/>                                               |
| [**Ianalysisregion**](ianalysisregion.md)                   | Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.<br/>                                                                                                                    |
| [**Ianalysisstatus**](ianalysisstatus.md)                   | Stellt den Status des frei Hand Analyse Vorgangs dar, indem beschrieben wird, ob die Analyse erfolgreich abgeschlossen wurde und ob Warnungen aufgetreten sind.<br/>                                                  |
| [**Ianalysiswarning**](ianalysiswarning.md)                 | Stellt eine Warnung oder einen Fehler dar, die während eines frei Hand Analyse Vorgangs auftritt.<br/>                                                                                                                           |
| [**Ianalysiswarning**](ianalysiswarnings.md)               | Enthält eine Auflistung von-Objekten, die die [**ianalysiswarning**](ianalysiswarning.md) -Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.<br/>                                      |
| [**Icontextlink**](icontextlink.md)                         | Stellt eine Beziehung zwischen zwei [**icontextnode**](icontextnode.md) -Objekten dar.<br/>                                                                                                                   |
| [**Icontextlinks**](icontextlinks.md)                       | Enthält eine Auflistung von-Objekten, die die [**icontextlink**](icontextlink.md) -Schnittstelle implementieren.<br/>                                                                                                   |
| [**Icontextnode**](icontextnode.md)                         | Stellt einen Knoten in einer Struktur von Objekten dar, die als Teil der frei Hand Analyse erstellt werden.<br/>                                                                                                                      |
| [**Icontextnodes**](icontextnodes.md)                       | Enthält eine Auflistung von-Objekten, die die [**icontextnode**](icontextnode.md) -Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.<br/>                                              |
| [**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)     | Ermöglicht den Zugriff auf Handschrift erkennungsungen für die Verwendung mit der Ink-Analyse.<br/>                                                                                                                                 |
| [**Iinkanalysiserkenzers**](iinkanalysisrecognizers.md)   | Enthält eine Auflistung von-Objekten, die die [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Schnittstelle implementieren und die die Fähigkeit zum Erkennen von Handschrift, Objekten oder Gesten darstellen.<br/> |
| [**Iinkanalyzer**](iinkanalyzer.md)                         | Bietet Zugriff auf Layoutanalyse, schreiben und Zeichnen von Klassifizierungen und Handschrifterkennung.<br/>                                                                                                  |
| [**Imatcheskriteriacallback**](imatchescriteriacallback.md) | Macht eine Methode verfügbar, um auszuwerten, ob ein [**icontextnode**](icontextnode.md) -Objekt bestimmte Kriterien erfüllt oder nicht.<br/>                                                                              |



 

## <a name="return-values"></a>Rückgabewerte

Methoden in der Tablet PC-COM-Bibliothek geben Werte von **HRESULT** zurück. Sofern nicht anders angegeben, werden die Bedeutungen der **HRESULT** -Werte in dieser Tabelle beschrieben.



| HRESULT-Wert                                   | BESCHREIBUNG                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Erfolg.<br/>                                                                      |
| E- \_ Zeiger<br/>                           | Mindestens ein Zeiger (entweder für einen Eingabe-oder einen Output-Parameter) ist ungültig.<br/> |
| E \_ invalidArg<br/>                        | Der Member hat versucht, ein ungültiges Argument zu übergeben.<br/>                              |
| E- \_ Ink- \_ Ausnahme<br/>                    | Ausnahme.<br/>                                                           |
| E \_ outo-Memory<br/>                       | Das System kann keinen Arbeitsspeicher zuweisen, um den Vorgang abzuschließen.<br/>                      |
| E \_ fehlschlagen<br/>                              | Ein nicht spezifizierter Fehler ist aufgetreten.<br/>                                                 |
| E \_ InvalidOperation<br/>                  | Der Member hat versucht, einen ungültigen Vorgang zu verwenden.<br/>                                 |
| TPC \_ E \_ ungültiger \_ Modus<br/>                | Der Member hat versucht, einen ungültigen Modus zu verwenden.<br/>                                      |
| TPC \_ E \_ - \_ Konfiguration ungültig<br/>       | Der Member hat versucht, eine ungültige Konfiguration zu verwenden.<br/>                             |
| TPC \_ E \_ ungültige \_ Paket \_ Beschreibung<br/> | Der Member hat versucht, eine ungültige Paketbeschreibung zu verwenden.<br/>                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




