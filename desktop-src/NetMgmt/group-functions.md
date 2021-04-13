---
title: Gruppenfunktionen
description: Eine globale Gruppe enthält Benutzerkonten aus einer Domäne, die unter einem Gruppenkonto Namen gruppiert sind.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390839"
---
# <a name="group-functions"></a>Gruppenfunktionen

Eine *globale Gruppe* enthält Benutzerkonten aus einer Domäne, die unter einem Gruppenkonto Namen gruppiert sind. Eine globale Gruppe kann nur Mitglieder (Benutzer) aus der Domäne enthalten, in der die globale Gruppe erstellt wird. Er darf keine lokalen Gruppen enthalten. Eine globale Gruppe ist innerhalb ihrer eigenen Domäne und innerhalb einer vertrauenden Domäne verfügbar.

Die Funktionen der Netzwerk Verwaltungsgruppe steuern globale Gruppen. Die Gruppenfunktionen sind nachfolgend aufgeführt.



| Funktion                                     | BESCHREIBUNG                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**"NetGroupAdd"**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Erstellt eine globale Gruppe.                                                           |
| [**Netgroupadduser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Fügt einer vorhandenen globalen Gruppe einen Benutzer hinzu.                                        |
| [**Netgroupdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Entfernt eine globale Gruppe, unabhängig davon, ob die Gruppe über Mitglieder verfügt.                  |
| [**Netgroupdelta User**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Entfernt einen Benutzernamen aus einer globalen Gruppe.                                        |
| [**Netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Listet alle globalen Gruppen auf einem Server auf.                                              |
| [**Netgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Gibt Informationen zu einer bestimmten globalen Gruppe zurück.                              |
| [**Netgroupgetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Listet alle Mitglieder einer bestimmten globalen Gruppe auf.                                   |
| [**Netgroupeintinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Legt allgemeine Informationen zu einer globalen Gruppe fest.                                    |
| [**Netgroupsetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Weist Mitglieder einer neuen globalen Gruppe zu. ersetzt die Mitglieder einer vorhandenen Gruppe. |



 

Wenn Sie die [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) -Funktion aufrufen, um eine globale Gruppe zu erstellen, müssen Sie einen Gruppennamen angeben. Anfänglich hat eine neue Gruppe keine Mitglieder.

Benutzerkonten gehören automatisch zu den speziellen globalen Gruppen Domänen Benutzern. Die Mitgliedschaft in dieser Gruppe wird indirekt von den Funktionen " [**nettuseradd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)", " [**nettuserdel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)" und " [**nettusersetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) " gesteuert.

Informationen zu globalen Gruppenkonten sind auf folgenden Ebenen verfügbar:

-   [**Gruppen \_ Informationen \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**Gruppen \_ Informationen \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**Gruppen \_ Informationen \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**Gruppen \_ Informationen \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**Gruppen \_ Informationen \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**Gruppen \_ Informationen \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

Die 1002-und 1005-Ebenen sind nur für die [**netgroupsetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) -Funktion gültig.

Informationen zu globalen Gruppenmitgliedern sind auf der folgenden Informationsebene verfügbar:

-   [**Gruppen \_ Benutzer \_ Informationen \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

Weitere Informationen finden Sie in den Funktionen der [lokalen](local-group-functions.md)Netzwerk Verwaltungsgruppe.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungsgruppe erreichen können. Weitere Informationen finden Sie unter [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 