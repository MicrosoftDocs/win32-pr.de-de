---
title: Code Dateien für das Beispiel des Quell Anbieters
description: Code Dateien für das Beispiel des Quell Anbieters
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Windows Media Device Manager, Dienstanbieter Beispiel
- Beispiel für Device Manager, Dienstanbieter
- Dienstanbieter, Beispiele
- Beispiele, Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100726"
---
# <a name="code-files-for-the-source-provider-sample"></a>Code Dateien für das Beispiel des Quell Anbieters

Das Beispiel Quell Anbieter Projekt enthält die folgenden Quell Code Dateien mit zugeordneten Headern:



| Datei                   | BESCHREIBUNG                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch. cpp            | Schließt Standard-ATL-Dateien ein.                                                                                                                                                                                    |
| Schlüssel. c                  | Enthält einen dummyauthentifizierungsschlüssel.                                                                                                                                                                            |
| loghelp. cpp            | Enthält Funktionen, die Aktivitäten und Fehler mithilfe der **wmdmlogger** -Klasse protokollieren, die in der WMDMLOG.dll Systemdatei implementiert ist.                                                                         |
| Mdserviceprovider. cpp  | Implementiert die cmdserviceprovider-Klasse, die die [**imdserviceprovider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) -und die icomponentauthenticate-Schnittstelle implementiert.                                                             |
| mdsp. cpp               | Der DLL-Einstiegspunkt und der Registrierungscode.                                                                                                                                                                          |
| Mdspdevice. cpp         | Implementiert eine Klasse, cmdspdevice, die die Schnittstellen [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**imdspdevicecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)und **ISpecifyPropertyPages** implementiert.                          |
| Mdspenum Device. cpp     | Implementiert die Klasse "cmdspenum Device", die die [**imdspenumschlag Device**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) -Schnittstelle implementiert.                                                                                                  |
| Mdspenum Storage. cpp    | Implementiert eine Klasse, cmdspenumschlag Storage, die die [**imdspenumschlag Storage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) -Schnittstelle implementiert.                                                                                               |
| Mdspstorage. cpp        | Implementiert eine Klasse, cmdspstorage, die die Schnittstellen [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**imdspobjectinfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)und [**imdspobject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) implementiert.                    |
| Mdspstorageglobals. cpp | Implementiert eine Klasse, cmdspstorageglobals, die die [**imdspstorageglobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) -Schnittstelle implementiert.                                                                                      |
| Mdsputil. cpp           | Enthält verschiedene Hilfsprogrammfunktionen für die Verwaltung von Geräten und Dateien.                                                                                                                                              |
| PropPage. cpp           | Implementiert eine Klasse, CPropPage, die die ATL-Klassen **IPropertyPageImpl** (zum Implementieren von IPropertyPage) und **CDialogImpl** erbt, die die ATL-Klasse CDialogImpl erbt (zum Verwalten von Fenstern und Nachrichten). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel Dienstanbieter**](sample-service-provider.md)
</dt> </dl>

 

 




