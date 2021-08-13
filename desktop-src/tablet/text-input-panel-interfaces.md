---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen, die zum Steuern der Darstellung und des Verhaltens des Tablet PC-Eingabebereichs verwendet werden.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Schnittstellen des Texteingabebereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2dcffe1eb67f00b4fe4d2ed3f371af003e040a30213516ae93eab73def6ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715406"
---
# <a name="text-input-panel-interfaces"></a>Schnittstellen des Texteingabebereichs

Dieser Abschnitt enthält Informationen zu den Schnittstellen, die zum Steuern der Darstellung und des Verhaltens des Tablet PC-Eingabebereichs verwendet werden.

> [!Note]  
> Die Schnittstellen des Texteingabebereichs sind nicht automatisierungskonform.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IHandWrittenTextInsertion-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Wird vom benutzerdefinierten Texteintragscode der Anwendung verwendet, um den Text sowohl in das Textfeld als auch in den Text services-Backing-Store zu einfügen.<br/> |
| [**ITextInputPanel-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Ermöglicht die Steuerung des Tablet PC-Eingabebereichs.<br/>                                                                                  |
| [**ITextInputPanelEventSink-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Definiert Methoden, die die [**ITextInputPanel-Schnittstellenereignisse**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) behandeln.<br/>                                      |
| [**ITextInputPanelRunInfo-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Stellt eine Methode zur Ermittlung zur Ermittlung der ausführungs aktuell ausgeführten Texteingabebereichs zur<br/>                                                      |
| [**ITipAutocompleteClient-Schnittstelle**](itipautocompleteclient.md)       | Ermöglicht dem Client das Aufrufen des Anbieterobjekts für den automatischen Abschluss des Texteingabebereichs der Anwendung.<br/>                                      |
| [**ITipAutocompleteProvider-Schnittstelle**](itipautocompleteprovider.md)   | Verwaltet die Anwendungsseite der automatischen Integration des Texteingabebereichs.<br/>                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 




