---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen, die verwendet werden, um die Darstellung und das Verhalten des Tablet PC-Eingabe Bereichs zu steuern.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Schnittstellen für Text Eingabebereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218352"
---
# <a name="text-input-panel-interfaces"></a>Schnittstellen für Text Eingabebereich

Dieser Abschnitt enthält Informationen zu den Schnittstellen, die verwendet werden, um die Darstellung und das Verhalten des Tablet PC-Eingabe Bereichs zu steuern.

> [!Note]  
> Die Schnittstellen für den Text Eingabebereich sind nicht Automation-kompatibel.

 

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ihandwrite-textinsertion-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Wird vom benutzerdefinierten Texteingabe Code der Anwendung verwendet, um den Text in das Textfeld und den Text Dienste-Unterstützungs Speicher einzufügen.<br/> |
| [**Itextinputpanel-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Bietet Kontrolle über den Tablet PC-Eingabebereich.<br/>                                                                                  |
| [**Itextinputpaneleventsink-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Definiert Methoden, die die [**itextinputpanel-Schnittstellen**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) Ereignisse behandeln.<br/>                                      |
| [**Itextinputpanelruninfo-Schnittstelle**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Stellt eine Methode bereit, um zu bestimmen, ob der Text Eingabebereich gerade ausgeführt wird.<br/>                                                      |
| [**Itipauwebcompleteclient-Schnittstelle**](itipautocompleteclient.md)       | Ermöglicht dem Client, das Auto Vervollständigen-Anbieter Objekt der Anwendung für den Text Eingabebereich aufzurufen.<br/>                                      |
| [**Itipauescompleteprovider-Schnittstelle**](itipautocompleteprovider.md)   | Verwaltet die Seite der Anwendung der automatischen vollständigen Integration des Text Eingabe Bereichs.<br/>                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 




