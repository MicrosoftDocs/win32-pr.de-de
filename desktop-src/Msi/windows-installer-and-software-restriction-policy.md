---
description: Windows Das Installationsprogramm ist in die Softwareeinschränkungsrichtlinie in Microsoft Windows XP integriert.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Richtlinie für Installationsprogramm und Softwareeinschränkung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e96d1c422b38fd82110cac34953f24be39909eeb64fa2236d3a993925a55c6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786560"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Richtlinie für Installationsprogramm und Softwareeinschränkung

Windows Das Installationsprogramm ist in die Softwareeinschränkungsrichtlinie in Microsoft Windows XP integriert. Die Richtlinie für Softwareeinschränkung kann über eine Gruppenrichtlinie konfiguriert werden. Mit der Softwareeinschränkungsrichtlinie kann ein Administrator sowohl Administratoren als auch Nichtadministratoren die Ausführung von Dateien basierend auf den Kriterien für Pfad, URL-Zone, Hash oder Herausgeber einschränken. Die Softwareeinschränkungsrichtlinie verfügt über zwei Ebenen: uneingeschränkt und nicht möglich. Der Windows Installer installiert nur Pakete, die auf uneingeschränkter Ebene ausgeführt werden dürfen.

Patches oder Transformationen müssen auch auf uneingeschränkter Ebene ausgeführt werden können. Wenn ein Paket, ein Patch oder eine Transformation so konfiguriert ist, dass es auf einer anderen Ebene als uneingeschränkt ausgeführt wird, zeigt der Windows-Installer eine Fehlermeldung an und protokolliert einen Eintrag im Anwendungsereignisprotokoll. Softwareeinschränkungsrichtlinie wird ausgewertet, wenn eine Anwendung zum ersten Mal installiert wird, wenn ein neuer Patch angewendet wird und das Installationspaket erneut zwischengespeichert wird.

Wenn ein Paket, ein Patch oder eine Transformation eingeschränkt ist, zeigt [](event-logging.md) der Windows Installer eine Fehlermeldung an und schreibt einen Eintrag für die Ereignisprotokollierung in das Anwendungsereignisprotokoll. Softwareeinschränkungsrichtlinie wird ausgewertet, wenn eine Anwendung zum ersten Mal installiert wird, wenn ein neuer Patch angewendet wird und das Installationspaket erneut zwischengespeichert wird.

Weitere Informationen zur Softwareeinschränkungsrichtlinie finden Sie in der Produktdokumentation, und [suchen Sie auf der TechNet-Website](https://www.microsoft.com/technet/sitemap.mspx).

 

 



