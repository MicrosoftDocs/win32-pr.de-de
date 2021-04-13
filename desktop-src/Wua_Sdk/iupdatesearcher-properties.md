---
description: Die iupdatesearcher-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Iupdatesearcher-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2021
ms.locfileid: "104354018"
---
# <a name="iupdatesearcher-properties"></a>Iupdatesearcher-Eigenschaften

Die [**iupdatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canautomaticallyupgradeservice**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Ruft einen booleschen Wert ab, der angibt, ob zukünftige Aufrufe der [**beginsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) -Methode und der [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) -Methode zu einem automatischen Upgrade auf Windows Update-Agent (WUA) führen, oder legt diesen fest. |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifiziert die aktuelle Client Anwendung.                                                                                                                                                                                                   |
| [**Incluabpotenziallyablösung dedupdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Ruft einen booleschen Wert ab, der angibt, ob die Suchergebnisse Updates enthalten, die durch andere Updates in den Suchergebnissen abgelöst werden, oder legt diesen fest.                                                                                          |
| [**Online**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Ruft einen booleschen Wert ab, der angibt, ob [**updatesearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) online geschaltet wird, um nach Updates zu suchen, oder legt diesen fest.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Dient zum Abrufen und Festlegen einer Site, die durchsucht werden soll, wenn es sich bei der zu suchenden Site nicht um Windows Update                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Dient zum Abrufen und Festlegen eines Server [**Auswahl**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) Werts, der den Server angibt, auf dem nach Updates gesucht werden soll.                                                                                                                            |




 

 

 



