---
title: Anforderungen an Netzwerk Verwaltungsfunktionen auf Servern und Arbeitsstationen
description: Wenn Sie eine der in diesem Thema aufgeführten Netzwerk Verwaltungsfunktionen auf einem Server oder einer Arbeitsstation aufrufen, gelten für Informations Abfragen und Informations Aktualisierungen andere Zugriffs Anforderungen.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858428"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>Anforderungen an Netzwerk Verwaltungsfunktionen auf Servern und Arbeitsstationen

Wenn Sie eine der in diesem Thema aufgeführten Netzwerk Verwaltungsfunktionen auf einem Server oder einer Arbeitsstation aufrufen, gelten für Informations Abfragen und Informations Aktualisierungen andere Zugriffs Anforderungen.

## <a name="queries"></a>Abfragen

Wenn Sie eine der folgenden Funktionen zum Ausführen einer Abfrage auf einem Server oder einer Arbeitsstation aufzurufen, können alle authentifizierten Benutzer standardmäßig die Informationen lesen und auflisten.

-   [**Netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**netgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**netgroupgetusers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**Netlocalgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**netlocalgroupgetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**netlocalgroupgetmembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   " [**Nettessiongetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) " (nur Stufen 1 und 2)
-   [**Netshareaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (nur Ebenen 2 und 502)
-   " [**Nettuserenum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)", " [**nettusergetgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)", " [**nettusergetinfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)", " [**nettusergetlocalgroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups)", " [**nettusermodalsget**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) "
-   [**Netwkstagetinfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **netwkstausererium**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Im folgenden finden Sie weitere Informationen über den anonymen Zugriff beim Lesen und Auflisten von Informationen.

**Windows Server 2003 und Windows XP:** Anonymer Zugriff auf Informationen ist möglich, wenn die Richtlinien Einstellung "everyoneincludesanall" den anonymen Zugriff zulässt.

**Windows 2000:** Der anonyme Zugriff auf Sicherungs fähige Objekte ist möglich, wenn die einschränier Bare Richtlinien Einstellung anonymen Zugriff zulässt. Sie können den anonymen Zugriff einschränken, indem Sie den folgenden Schlüssel in der Registrierung auf den Wert 1 festlegen.

**HKEY \_ Lokales \_ Computer \\ System \\ CurrentControlSet \\ Control \\ LSA** \\ **restrictanfts=** 1

Weitere Informationen finden Sie im folgenden Artikel in der Microsoft Knowledge Base:

Artikel-ID: [Q246261](https://support.microsoft.com/kb/246261)

Title: Verwenden des einschrändenden Registrierungs Werts.

## <a name="updates"></a>Aktualisierungen

Standardmäßig können nur Administratoren und Hauptbenutzer Informationen schreiben.

Weitere Informationen zum Steuern des Zugriffs auf Sicherungs fähige Objekte finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control), [Berechtigungen](/windows/desktop/SecAuthZ/privileges)und Sicherungs [fähige Objekte](/windows/desktop/SecAuthZ/securable-objects). Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

 

 