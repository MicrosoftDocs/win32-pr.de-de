---
title: Herunterfahren eines Multicast-Routing Protokolls
description: In der folgenden Tabelle werden eine Reihe von Schritten für das Herunterfahren der Interaktion zwischen dem Multicast-Gruppen-Manager und dem Routing Protokoll zusammengefasst, wenn das Routing Protokoll heruntergefahren wird.
ms.assetid: d868218d-7939-45d1-9e2f-3415c40f1a62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d35285bdf613cb8ec5966fa438742004a97c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729328"
---
# <a name="shutting-down-a-multicast-routing-protocol"></a>Herunterfahren eines Multicast-Routing Protokolls

In der folgenden Tabelle werden eine Reihe von Schritten für das Herunterfahren der Interaktion zwischen dem Multicast-Gruppen-Manager und dem Routing Protokoll zusammengefasst, wenn das Routing Protokoll heruntergefahren wird. In der ersten Spalte werden die Aktionen beschrieben, die das Routing Protokoll ausführt, und die Antwort des Routing Protokolls an den Multicast-Gruppen-Manager. In der zweiten Spalte werden die Antworten des Multicast Gruppen-Managers auf das Routing Protokoll und alle Aktionen beschrieben, die der Multicast-Gruppen-Manager ausführt, z. b. Rückrufe. Die dritte Spalte enthält alle zusätzlichen Informationen.

Jede Zeile der Tabelle stellt einen Schritt dar.



| Routing Protokoll Aktion                                                                                                                                     | Multicast-Gruppen-Manager-Aktion                                                                                                                                                                                                                                                                                                                                                                                                                                            | Notizen                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Freigabe Besitz für jede Schnittstelle, die das Routing Protokoll besitzt, mithilfe der [**mgmreleaseingeterfaceownership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership) -Funktion. | Wenn IGMP auch auf der Schnittstelle ausgeführt wird, die gerade von einem Routing Protokoll freigegeben wurde, wenden Sie sich an IGMP, indem Sie den [**pmgm- \_ \_ \_ Rückruf Rückruf deaktivieren**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . Nachdem alle Änderungen an Multicast Daten bezüglich Schnittstellen Besitz vorgenommen wurden, wenden Sie sich erneut an IGMP. verwenden Sie hierzu pmgm, um den [**\_ \_ IGMP- \_ Rückruf**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) Rückruf zu aktivieren<br/> Löschen Sie alle Weiterleitungs Einträge, die dieser Schnittstelle zugeordnet sind.<br/> |                                                                           |
| Registrieren Sie sich beim Multicast-Gruppen-Manager mithilfe der [**mgmderegistermprotocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) -Funktion.                                    | Zerstören Sie das Handle, das durch einen vorherigen Aufrufen der [**mgmderegistermprotocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) -Funktion an das Routing Protokoll zurückgegeben wurde.                                                                                                                                                                                                                                                                                                                 | Das Routing Protokoll kann dieses Handle nicht mehr verwenden, um die MGM-Funktionen aufzurufen. |



 

 

