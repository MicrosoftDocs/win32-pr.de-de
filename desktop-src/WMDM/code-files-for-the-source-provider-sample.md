---
title: Codedateien für das Quellanbieterbeispiel
description: Codedateien für das Quellanbieterbeispiel
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Medien Geräte-Manager,Beispiele
- Geräte-Manager,Beispiele
- Windows Medien Geräte-Manager,Beispiel für Dienstanbieter
- Geräte-Manager,Dienstanbieterbeispiel
- Dienstanbieter,Beispiele
- Beispiele,Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c29127aebea6898868b29adb17a15c8d174e1fedfd3228bd565bf8ef4ce9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586367"
---
# <a name="code-files-for-the-source-provider-sample"></a>Codedateien für das Quellanbieterbeispiel

Das Beispiel-Quellanbieterprojekt enthält die folgenden Quellcodedateien mit zugeordneten Headern:



| Datei                   | BESCHREIBUNG                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch.cpp            | Enthält ATL-Standarddateien.                                                                                                                                                                                    |
| key.c                  | Enthält einen Dummyauthentifizierungsschlüssel.                                                                                                                                                                            |
| loghelp.cpp            | Enthält Funktionen, die Aktivität und Fehler mithilfe der **WMDMLogger-Klasse** protokollieren, die in der WMDMLOG.dll implementiert ist.                                                                         |
| MDServiceProvider.cpp  | Implementiert die Klasse CMDServiceProvider, die die [**Schnittstellen IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) und IComponentAuthenticate implementiert.                                                             |
| mdsp.cpp               | DLL-Einstiegspunkt und Registrierungscode.                                                                                                                                                                          |
| MDSPDevice.cpp         | Implementiert die Klasse CMDSPDevice, die die [**Schnittstellen IMDSPDevice2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2) [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)und **ISpecifyPropertyPages** implementiert.                          |
| MDSPEnumDevice.cpp     | Implementiert die Klasse CMDSPEnumDevice, die die [**IMDSPEnumDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) implementiert.                                                                                                  |
| MDSPEnumStorage.cpp    | Implementiert die Klasse CMDSPEnumStorage, die die [**IMDSPEnumStorage-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) implementiert.                                                                                               |
| MDSPStorage.cpp        | Implementiert die Klasse CMDSPStorage, die die [**Schnittstellen IMDSPStorage2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2) [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)und [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) implementiert.                    |
| MDSPStorageGlobals.cpp | Implementiert die Klasse CMDSPStorageGlobals, die die [**IMDSPStorageGlobals-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) implementiert.                                                                                      |
| MDSPutil.cpp           | Enthält verschiedene Hilfsfunktionen für die Geräte- und Dateiverwaltung.                                                                                                                                              |
| proppage.cpp           | Implementiert die Klasse CPropPage, die die ATL-Klassen **IPropertyPageImpl** (zum Implementieren von IPropertyPage) und **CDialogImpl** erbt, die die ATL-Klasse CDialogImpl (zum Verwalten von Fenstern und Nachrichten) erbt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel-Dienstanbieter**](sample-service-provider.md)
</dt> </dl>

 

 




