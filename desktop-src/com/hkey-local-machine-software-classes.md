---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Die Unterschlüssel und Registrierungswerte, die dem Schlüssel HKEY LOCAL MACHINE SOFTWARE Classes zugeordnet sind, enthalten Informationen zu einer Anwendung, die zur Unterstützung der \_ \_ \\ \\ COM-Funktionalität erforderlich ist.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9a79c417c48c5392fe5ceea3e99cce5e874bc9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884874"
---
# <a name="hkey_local_machinesoftwareclasses"></a>HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Classes

Die Unterschlüssel und Registrierungswerte, die dem Schlüssel **HKEY \_ LOCAL MACHINE SOFTWARE \_ \\ \\ Classes** zugeordnet sind, enthalten Informationen zu einer Anwendung, die zur Unterstützung der COM-Funktionalität erforderlich ist. Diese Informationen umfassen Themen wie unterstützte Datenformate, Kompatibilitätsinformationen, programmgesteuerte Bezeichner, DCOM und Steuerelemente.



| Unterschlüssel                                                                         | Beschreibung                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**Appid**](appid-key.md)                                                     | Konfigurationsoptionen für COM-basierte Anwendungen.                                                                 |
| [**CLSID**](clsid-key-hklm.md)                                                | Konfigurationsoptionen für COM-Klassen.                                                                            |
| [**<\_ Dateierweiterung>**](-file-extension--key.md)                        | Ordnet einer ProgID eine Dateinamenerweiterung zu.                                                                   |
| [**FileType**](filetype-key.md)                                               | Wird von [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet, um Muster mit verschiedenen Dateibytes in einer nicht zusammengesetzten Datei abzugleichen. |
| [**Schnittstelle**](interface-key.md)                                             | Ordnet einen Schnittstellennamen einer Schnittstellen-ID (IID) zu.                                                          |
| [**&lt;ProgID&gt;**](-progid--key.md)                                         | Identifiziert eine Klasse. Beachten Sie, dass die ProgID im Gegensatz zu einer CLSID nicht garantiert global eindeutig ist.                 |
| [**<versionsunabhängige ProgID->**](-version-independent-progid--key.md) | Wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen.                                                    |



 

 

 




