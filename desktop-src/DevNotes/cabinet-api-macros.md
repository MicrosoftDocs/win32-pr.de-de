---
description: Weitere Informationen finden Sie in den CAB-API-Makros.
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: CAB-API-Makros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522867"
---
# <a name="cabinet-api-macros"></a>CAB-API-Makros

In diesem Abschnitt werden die von der CAB-API verwendeten Makros ausführlich erläutert:

## <a name="fci-macros"></a>FCI-Makros

Die folgenden Makros werden von FCI verwendet:



| Makro                                              | Beschreibung                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNF-Zuordnung**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Wird verwendet, um Arbeitsspeicher in einem FCI-Kontext zuzuordnen.<br/>                                          |
| [**Fnficiclose**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Wird verwendet, um eine Datei zu schließen.<br/>                                                               |
| [**Fnficidelete**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Wird verwendet, um eine Datei zu löschen.<br/>                                                              |
| [**FNF-Datei platziert**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Wird verwendet, um zu benachrichtigen, wenn eine Datei in der CAB-Datei platziert wird.<br/>                                |
| [**FNF-frei**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Wird verwendet, um zuvor zugeordneten Speicher in einem FCI-kontextfrei zugeben.<br/>                         |
| [**Fnscigetnextcabinet**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Wird verwendet, um Informationen für den nächsten Schrank anzufordern.<br/>                                   |
| [**FNF-getopeninfo**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Wird verwendet, um eine Datei zu öffnen und Datum, Uhrzeit und Attribute der Datei abzurufen.<br/>                   |
| [**Fnficigettempfile**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Wird zum Abrufen eines temporären Datei namens verwendet.<br/>                                               |
| [**FNF-offen**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Wird zum Öffnen einer Datei in einem FCI-Kontext verwendet.<br/>                                              |
| [**FNF-Lesevorgänge**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Wird zum Lesen von Daten aus einer Datei verwendet.<br/>                                                      |
| [**FNF-Seek**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Wird verwendet, um einen Dateizeiger an eine angegebene Position zu verschieben.<br/>                                |
| [**Fnfcistatus**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Wird verwendet, um den Benutzer zu aktualisieren.<br/>                                                            |
| [**FNF schreiben**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Wird verwendet, um Daten in eine Datei zu schreiben.<br/>                                                       |
| [**Tcompfromlzxwindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Konvertiert die Windows-Größe in einen lxz-tcomp-Wert für " [**sciaddfile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)".<br/> |



 

## <a name="fdi-macros"></a>FDI-Makros

Die folgenden Makros werden von FDI verwendet:



| Makro                              | Beschreibung                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**Fnzuweisung**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Wird verwendet, um Speicher in einem FDI-Kontext zuzuordnen.<br/>                               |
| [**Fnclose**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Wird verwendet, um eine Datei in einem FDI-Kontext zu schließen.<br/>                                  |
| [**Fnodinotifizieren**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Wird verwendet, um die Anwendung auf den Status des Decoders zu aktualisieren.<br/>             |
| [**Fnfree**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Wird verwendet, um zuvor zugeordneten Speicher in einem FDI-kontextfrei zugeben.<br/>              |
| [**Fnopen**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Wird zum Öffnen einer Datei in einem FDI-Kontext verwendet.<br/>                                   |
| [**Fnread**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Wird zum Lesen von Daten aus einer Datei in einem FDI-Kontext verwendet.<br/>                         |
| [**Fnseek**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Wird verwendet, um einen Dateizeiger an die angegebene Position in einem FDI-Kontext zu verschieben.<br/> |
| [**Fnwrite**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Wird verwendet, um Daten in eine Datei in einem FDI-Kontext zu schreiben.<br/>                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CAB-API-Referenz](cabinet-api-reference.md)
</dt> <dt>

[Verwenden der CAB-API](using-the-cabinet-api.md)
</dt> </dl>

 

 




