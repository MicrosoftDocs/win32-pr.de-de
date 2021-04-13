---
title: Plug-in-Strukturen
description: Strukturen für die Entwicklung von Client Anwendungen durch die Windows-Biometrieframework-API.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows-Biometrieframework API-Windows-Biometrieframework-API, Plug-in-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310876"
---
# <a name="plug-in-structures"></a>Plug-in-Strukturen

Die folgenden Strukturen werden für die Entwicklung von Client Anwendungen durch die Windows-Biometrieframework-API unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**winbio- \_ Konto \_ Richtlinie**](winbio-account-policy.md)<br/>                                  | Enthält entweder eine Standard-oder eine kontospezifische Antispoofing-Richtlinie.<br/>                                                         |
| [**winbio \_ Adapter \_ Interface- \_ Version**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Enthält eine Haupt-und neben Versionsnummer, die in den Tabellen-, Sensor-und Speicher Adapter-Schnittstellen Tabellen verwendet wird.<br/>                |
| [**winbio- \_ Engine- \_ Schnittstelle**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Enthält Zeiger auf die benutzerdefinierten Engine-Adapter Funktionen.<br/>                                                                 |
| [**Erweiterte winbio-Registrierungs \_ \_ \_ Parameter**](winbio-extended-enrollment-parameters.md)<br/> | Enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungs Vorlage benötigt. <br/>                            |
| [**winbio- \_ Pipeline**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Enthält freigegebene Kontextinformationen, die von den Sensor-, Engine-und Speicher Adapter Komponenten in einer einzelnen biometrischen Einheit verwendet werden.<br/> |
| [**winbio- \_ Sensor \_ Schnittstelle**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Enthält Zeiger auf die benutzerdefinierten Sensor Adapter Funktionen.<br/>                                                                 |
| [**winbio- \_ Speicher \_ Schnittstelle**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Enthält Zeiger auf die benutzerdefinierten Speicher Adapter Funktionen.<br/>                                                                |
| [**winbio- \_ Speicher \_ Daten Satz**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Enthält eine biometrische Vorlage und zugehörige Daten in einem Standardformat.<br/>                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-in-Referenz](plug-in-reference.md)
</dt> <dt>

[Plug-in-Funktionen](plug-in-functions.md)
</dt> <dt>

[**Wbioqueryengineinterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**Wbioquerysensorinterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**Wbioquerystorageinterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





