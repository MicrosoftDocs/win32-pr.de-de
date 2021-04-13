---
title: Zulässige Berechtigung zum Authentifizieren von erweiterten Rechten
description: Das Steuerelement Zugriffsrecht steuert, wer sich bei einem bestimmten Computer oder Dienst authentifizieren kann.
ms.assetid: 265e6240-0fb5-4037-8c66-05fadc646100
ms.tgt_platform: multiple
keywords:
- Das AD-Schema für erweiterte Rechte kann nicht authentifiziert werden.
topic_type:
- apiref
api_name:
- Allowed-To-Authenticate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2fca1b6f4670fd340170ed5cfd1f0160d61945
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480447"
---
# <a name="allowed-to-authenticate-extended-right"></a>Zulässige Berechtigung zum Authentifizieren von erweiterten Rechten

Das Steuerelement Zugriffsrecht steuert, wer sich bei einem bestimmten Computer oder Dienst authentifizieren kann. Sie befindet sich im Grunde auf Computern, Benutzern und inetOrgPerson-Objekten. Dies gilt auch für das Domänen Objekt, wenn der Zugriff für die gesamte Domäne zulässig ist. Sie kann auf Organisationseinheiten angewendet werden, um Benutzern die Möglichkeit zu geben, vererbbare ACEs auf Organisationseinheiten festzulegen, die eine Gruppe von Benutzer-oder Computer Objekten enthalten.



| Eingabe | Wert |
|--------------|--------------------------------------|
| CN           | Zulässig zu authentifizieren              |
| Anzeigename | Authentifizieren zulässig              |
| Rights-GUID  | 68b1d179-0d15-4d4f-ab71-46152e79a7bc |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierung-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierung-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierung-Display-ID | 65                                                                                                                              |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Konto**](c-msds-managedserviceaccount.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierung-Display-ID | 65                                                                                                                                                                                                               |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Konto**](c-msds-managedserviceaccount.md)<br/> [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> |
| Lokalisierung-Display-ID | 65                                                                                                                                                                                                               |



 

 





