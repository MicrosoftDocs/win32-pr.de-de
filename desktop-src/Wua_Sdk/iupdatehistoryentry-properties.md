---
description: Die IUpdateHistoryEntry-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: IUpdateHistoryEntry-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5c6951857f72f4a9ee4f86cd29d42e024e05b87d58d589043f5a40e951d4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738269"
---
# <a name="iupdatehistoryentry-properties"></a>IUpdateHistoryEntry-Eigenschaften

Die [**IUpdateHistoryEntry-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) definiert die folgenden Eigenschaften.



| Eigenschaft                                                               | Beschreibung                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Ruft den Bezeichner der Clientanwendung ab, die ein Update verarbeitet hat.                                                  |
| [**Date**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Ruft das Datum und die Uhrzeit der Anwendung eines Updates ab.                                                                        |
| [**Beschreibung**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Ruft die Beschreibung eines Updates ab.                                                                                       |
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Ruft den **HRESULT-Wert** ab, der vom Vorgang bei einem Update zurückgegeben wird.                                             |
| [**Vorgang**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Ruft einen [**UpdateOperation-Wert**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) ab, der den Vorgang für ein Update angibt.                      |
| [**Resultcode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Ruft einen [**OperationResultCode-Wert**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) ab, der das Ergebnis eines Vorgangs bei einem Update angibt. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Ruft den [**ServerSelection-Wert ab, der**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) angibt, welcher Server ein Update bereitgestellt hat.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Ruft den Dienstbezeichner eines Updatediensts ab, der kein Windows Update ist.                                           |
| [**Supporturl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Ruft einen Link zu den sprachspezifischen Unterstützungsinformationen für ein Update ab.                                             |
| [**Titel**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Ruft den Titel eines Updates ab.                                                                                             |
| [**DeinstallationNotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Ruft die Deinstallationshinweise eines Updates ab.                                                                              |
| [**DeinstallationSchritte**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Ruft die [**IStringCollection-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) ab, die die Deinstallationsschritte für ein Update enthält.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Ruft den nicht zugeordneten Ergebniscode ab, der von einem Vorgang bei einem Update zurückgegeben wird.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Ruft eine Zeichenfolge ab. Die Zeichenfolge enthält den eindeutigen Bezeichner eines Updates.                                                   |



 

 

 
