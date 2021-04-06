---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Die Unterschlüssel und Registrierungs Werte, die dem Schlüssel HKEY \_ Local Machine Classes zugeordnet sind, \_ \\ \\ enthalten Informationen zu einer Anwendung, die zur Unterstützung der com-Funktionalität benötigt wird.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714099"
---
# <a name="hkey_local_machinesoftwareclasses"></a>HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer

Die Unterschlüssel und Registrierungs Werte, die dem Schlüssel **HKEY \_ local \_ Machine \\ \\ Classes** zugeordnet sind, enthalten Informationen zu einer Anwendung, die zur Unterstützung der com-Funktionalität benötigt wird. Diese Informationen umfassen Themen wie Unterstützte Datenformate, Kompatibilitätsinformationen, programmgesteuerte Bezeichner, DCOM und Steuerelemente.



| Unterschlüssel                                                                         | BESCHREIBUNG                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid-key.md)                                                     | Konfigurationsoptionen für COM-basierte Anwendungen.                                                                 |
| [**CLSID**](clsid-key-hklm.md)                                                | Konfigurationsoptionen für COM-Klassen.                                                                            |
| [**<Datei \_ Erweiterung>**](-file-extension--key.md)                        | Ordnet eine Dateinamenerweiterung einer ProgID zu.                                                                   |
| [**FileType**](filetype-key.md)                                               | Wird von [**getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen. |
| [**Schnittstelle**](interface-key.md)                                             | Ordnet einen Schnittstellennamen einer Schnittstellen-ID (IID) zu.                                                          |
| [**<ProgID>**](-progid--key.md)                                         | Identifiziert eine Klasse. Beachten Sie, dass es im Gegensatz zu einer CLSID nicht garantiert wird, dass die ProgID global eindeutig ist.                 |
| [**<Versions unabhängige ProgID>**](-version-independent-progid--key.md) | Wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.                                                    |



 

 

 




