---
title: Erweitertes Recht "Allowed-To-Authenticate"
description: Das Zugriffssteuerungsrecht steuert, wer sich bei einem bestimmten Computer oder Dienst authentifizieren kann.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- AD-Schema mit erweiterter Berechtigung für die Authentifizierung
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446a63d63751105500986c27c7a851d60146a72281ee8415bc01c5ec8c5dfa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548830"
---
# <a name="allowed-to-authenticate-extended-right"></a>Erweitertes Recht "Allowed-To-Authenticate"

Das Zugriffssteuerungsrecht steuert, wer sich bei einem bestimmten Computer oder Dienst authentifizieren kann. Es befindet sich im Grunde auf Computer-, Benutzer- und InetOrgPerson-Objekten. Sie gilt auch für das Domänenobjekt, wenn der Zugriff für die gesamte Domäne zulässig ist. Sie kann auf Organisationseinheiten angewendet werden, damit Benutzer vererbbare ACEs für Organisationseinheiten festlegen können, die eine Reihe von Benutzer- oder Computerobjekten enthalten.



| Eingabe | Wert |
|--------------|--------------------------------------|
| CN           | Zulässige Authentifizierung              |
| Anzeigename | Authentifizierung zulässig              |
| Rechte-GUID  | 68b1d179-0d15-4d4f-ab71-46152e79a7bc |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierungsanzeige-ID | 65                                                                                                                              |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierungsanzeige-ID | 65                                                                                                                              |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierungsanzeige-ID | 65                                                                                                                              |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierungsanzeige-ID | 65                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierungsanzeige-ID | 65                                                                                                                                                                                                               |



 

 





