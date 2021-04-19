---
description: Die iupdatehistoryentry-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Iupdatehistoryentry-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3acdc9ed32c35028a253944d434c23231c5b6d
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2021
ms.locfileid: "106367339"
---
# <a name="iupdatehistoryentry-properties"></a>Iupdatehistoryentry-Eigenschaften

Die [**iupdatehistoryentry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                               | BESCHREIBUNG                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Ruft den Bezeichner der Client Anwendung ab, die ein Update verarbeitet hat.                                                  |
| [**Datum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Ruft das Datum und die Uhrzeit ab, zu der ein Update angewendet wurde.                                                                        |
| [**Beschreibung**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Ruft die Beschreibung eines Updates ab.                                                                                       |
| [**HRESULT**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Ruft den **HRESULT** -Wert ab, der vom-Vorgang bei einem Update zurückgegeben wird.                                             |
| [**Vorgang**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Ruft einen [**updateoperation**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) -Wert ab, der den Vorgang für ein Update angibt.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Ruft einen [**operationresultcode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) -Wert ab, der das Ergebnis eines Vorgangs bei einem Update angibt. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Ruft den [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) -Wert ab, der angibt, welcher Server ein Update bereitgestellt hat.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Ruft den Dienst Bezeichner eines Update dienstaners ab, der kein Windows-Update ist.                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Ruft einen Hyperlink zu den sprachspezifischen Unterstützungs Informationen für ein Update ab.                                             |
| [**Titel**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Ruft den Titel eines Updates ab.                                                                                             |
| [**Uninstallationnotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Ruft die uninstallationshinweise eines Updates ab.                                                                              |
| [**Uninstallationsteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Ruft die [**istringcollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) -Schnittstelle ab, die die uninstallations Schritte für ein Update enthält.  |
| [**Unmapperdresultcode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Ruft den nicht zugeordneten Ergebniscode ab, der bei einem Update von einem Vorgang zurückgegeben wird.                                           |
| [**UPDATEIDENTITY**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Ruft eine Zeichenfolge ab. Die Zeichenfolge enthält den eindeutigen Bezeichner eines Updates.                                                   |



 

 

 
