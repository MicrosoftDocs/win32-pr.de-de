---
description: 'Weitere Informationen finden Sie unter: Makros der Cabinet-API.'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Makros der Cabinet-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525ec84e3e857c4819b1689cade2ed0f7267dffbd8a0e0da02251a03f8d4a36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668268"
---
# <a name="cabinet-api-macros"></a>Makros der Cabinet-API

In diesem Abschnitt werden die makros beschrieben, die von der Cabinet-API verwendet werden:

## <a name="fci-macros"></a>FCI-Makros

Die folgenden Makros werden von FCI verwendet:



| Makro                                              | Beschreibung                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Wird verwendet, um Arbeitsspeicher in einem FCI-Kontext zu reservieren.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Wird verwendet, um eine Datei zu schließen.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Wird zum Löschen einer Datei verwendet.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Wird verwendet, um zu benachrichtigen, wenn eine Datei in der Schränkung platziert wird.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Wird verwendet, um zuvor zugewiesenen Arbeitsspeicher in einem FCI-Kontext frei zu geben.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Wird zum Anfordern von Informationen für das nächste Schränk verwendet.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Wird verwendet, um eine Datei zu öffnen und Datum, Uhrzeit und Attribute der Datei abzurufen.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Wird verwendet, um einen temporären Dateinamen zu erhalten.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Wird verwendet, um eine Datei in einem FCI-Kontext zu öffnen.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Wird zum Lesen von Daten aus einer Datei verwendet.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Wird verwendet, um einen Dateizeiger an einen angegebenen Speicherort zu verschieben.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Wird verwendet, um den Benutzer zu aktualisieren.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Wird zum Schreiben von Daten in eine Datei verwendet.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Konvertiert die Fenstergröße in einen LXZ-TCOMP-Wert für [**FCIAddFile.**](/windows/desktop/api/Fci/nf-fci-fciaddfile)<br/> |



 

## <a name="fdi-macros"></a>FDI-Makros

Die folgenden Makros werden von FDI verwendet:



| Makro                              | Beschreibung                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Wird verwendet, um Arbeitsspeicher in einem FDI-Kontext zu reservieren.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Wird verwendet, um eine Datei in einem FDI-Kontext zu schließen.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Wird verwendet, um die Anwendung auf den Status des Decoders zu aktualisieren.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Wird verwendet, um zuvor zugewiesenen Arbeitsspeicher in einem FDI-Kontext frei zu geben.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Wird verwendet, um eine Datei in einem FDI-Kontext zu öffnen.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Wird zum Lesen von Daten aus einer Datei in einem FDI-Kontext verwendet.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Wird verwendet, um einen Dateizeiger an den angegebenen Speicherort in einem FDI-Kontext zu verschieben.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Wird verwendet, um Daten in eine Datei in einem FDI-Kontext zu schreiben.<br/>                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Cabinet-API](cabinet-api-reference.md)
</dt> <dt>

[Verwenden der Cabinet-API](using-the-cabinet-api.md)
</dt> </dl>

 

 




