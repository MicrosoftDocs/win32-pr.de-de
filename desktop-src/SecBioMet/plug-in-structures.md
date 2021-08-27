---
title: Plug-In-Strukturen
description: Strukturen für die Clientanwendungsentwicklung durch die Windows Biometrieframework-API.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows Biometrieframework-API Windows Biometrieframework-API, Plug-In-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e150dd043a8c95e91d0f9095e23584544f43a503a709ae54c9180e06aa40bdaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101240"
---
# <a name="plug-in-structures"></a>Plug-In-Strukturen

Die folgenden Strukturen werden für die Entwicklung von Clientanwendungen von der Windows Biometrieframework-API unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WINBIO-KONTORICHTLINIE \_**](winbio-account-policy.md)<br/>                                  | Enthält entweder eine Standardrichtlinie oder eine kontospezifische Antipoofingrichtlinie.<br/>                                                         |
| [**VERSION DER \_ \_ WINBIO-ADAPTERSCHNITTSTELLE \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Enthält eine Haupt- und Nebenversionsnummer, die in den Schnittstellentabellen für Engine, Sensor und Speicheradapter verwendet wird.<br/>                |
| [**\_WINBIO-ENGINE-SCHNITTSTELLE \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Enthält Zeiger auf ihre benutzerdefinierten Engine-Adapterfunktionen.<br/>                                                                 |
| [**PARAMETER FÜR DIE \_ ERWEITERTE WINBIO-REGISTRIERUNG \_ \_**](winbio-extended-enrollment-parameters.md)<br/> | Enthält zusätzliche Informationen, die ein Engine-Adapter zum Erstellen einer Registrierungsvorlage benötigt. <br/>                            |
| [**\_WINBIO-PIPELINE**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Enthält freigegebene Kontextinformationen, die von den Sensor-, Engine- und Speicheradapterkomponenten in einer einzelnen biometrischen Einheit verwendet werden.<br/> |
| [**\_WINBIO-SENSORSCHNITTSTELLE \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Enthält Zeiger auf Ihre benutzerdefinierten Sensoradapterfunktionen.<br/>                                                                 |
| [**\_WINBIO-SPEICHERSCHNITTSTELLE \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Enthält Zeiger auf Ihre benutzerdefinierten Speicheradapterfunktionen.<br/>                                                                |
| [**\_ \_ WINBIO-SPEICHERDATENSATZ**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Enthält eine biometrische Vorlage und zugehörige Daten in einem Standardformat.<br/>                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-In-Referenz](plug-in-reference.md)
</dt> <dt>

[Plug-In-Funktionen](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





