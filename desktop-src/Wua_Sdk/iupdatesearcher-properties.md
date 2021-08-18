---
description: Die IUpdateSearcher-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: IUpdateSearcher-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dc3af2635fff4260a44261333b23cbfcf1661793ad613f08bb288db452b93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130432"
---
# <a name="iupdatesearcher-properties"></a>IUpdateSearcher-Eigenschaften

Die [**IUpdateSearcher-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                           | Beschreibung                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Ruft einen booleschen Wert ab, der angibt, ob zukünftige Aufrufe der [**Methoden BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) und [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) zu einem automatischen Upgrade auf Windows Update-Agent (WUA) führen, und legt diesen fest. |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifiziert die aktuelle Clientanwendung.                                                                                                                                                                                                   |
| [**IncludePerslySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Ruft einen booleschen Wert ab, der angibt, ob die Suchergebnisse Updates enthalten, die von anderen Updates in den Suchergebnissen abgelöst werden, und legt diesen fest.                                                                                          |
| [**Online**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Ruft einen booleschen Wert ab, der angibt, ob [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) online geschaltet wird, um nach Updates zu suchen, und legt diesen fest.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Ruft einen zu durchsuchende Standort ab und legt diesen fest, wenn der zu durchsuchende Standort kein Windows Updatestandort ist.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Ruft einen [**ServerSelection-Wert**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) ab, der den Server angibt, nach Updates zu suchen, und legt diesen fest.                                                                                                                            |




 

 

 



