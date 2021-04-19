---
description: Network DDE verwendet vertrauenswürdige Freigaben und Sicherheits Deskriptoren zum Steuern des Zugriffs auf Freigaben.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Vertrauenswürdige Freigaben und Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899be51745b2b27c22212c3ceeaceea016fa8d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339735"
---
# <a name="trusted-shares-and-security"></a>Vertrauenswürdige Freigaben und Sicherheit

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Network DDE verwendet vertrauenswürdige Freigaben und Sicherheits Deskriptoren zum Steuern des Zugriffs auf Freigaben.

## <a name="trusted-shares"></a>Vertrauenswürdige Freigaben

Wenn ein Client Benutzer von einem Remote Computer aus eine Verbindung mit einer DDE-Freigabe herstellt, akzeptiert Network DDE die Anforderung nur, wenn die folgenden Aussagen zutreffen:

-   Der Benutzer, der die Freigabe erstellt hat, hat der Freigabe den vertrauenswürdigen Status erteilt, indem er [**nddesettrustedshare**](nddesettrustedshare.md)aufgerufen hat. Nur der Ersteller der Freigabe kann der Freigabe den vertrauenswürdigen Status gewähren. Nicht einmal ein Administrator kann einer DDE-Freigabe, die von einem anderen Benutzer erstellt wurde, den vertrauenswürdigen Status gewähren.
-   Der Benutzer, der die Freigabe erstellt hat, ist zurzeit beim Server Computer angemeldet.

Durch den Prozess der Gewährung eines vertrauenswürdigen Status an eine Freigabe wird die Freigabe der Liste der vertrauenswürdigen Freigaben des angemeldeten Benutzers in DSDM hinzugefügt. Dadurch wird eine Vertrauensstellung zwischen dem Server und seinen Clients erstellt. Wenn eine DDE-Freigabe den vertrauenswürdigen Status aufweist, können Clients eine Verbindung damit herstellen, solange der Benutzer, der die Freigabe erstellt hat, angemeldet ist. Wenn der Client von einem Remote Computer aus eine Verbindung mit der Freigabe herstellt, akzeptiert Netzwerk DDE die Anforderung nur dann, wenn die Freigabe in der Liste der vertrauenswürdigen Freigaben des angemeldeten Benutzers in DSDM aufgeführt ist.

## <a name="security"></a>Sicherheit

Network DDE führt eine zusätzliche Sicherheitsüberprüfung durch, wenn der Client Daten oder einen Link anfordert. Es wird überprüft, ob der Server dem Remote Benutzer die erforderliche Berechtigung für den Vorgang erteilt hat. Der Server steuert den Zugriff auf die Freigabe über den *pSD* -Parameter der [**ndabshareadd**](nddeshareadd.md) -Funktion. Dieser Parameter gibt die Sicherheits Beschreibung an. Wenn dieser Parameter **null** ist, erstellt die Funktion eine Standard Sicherheits Beschreibung, die uneingeschränkten Zugriff auf den Ersteller der Freigabe gewährt und allen anderen Benutzern Lese-und Verknüpfungs Berechtigungen erteilt. Erstellen und verwenden Sie eine Sicherheits Beschreibung, um einzelnen Benutzern oder Benutzergruppen zusätzliche Berechtigungen zu erteilen oder zu verweigern. Weitere Informationen zu Sicherheits Deskriptoren finden Sie unter [**Access Control**](/windows/desktop/SecAuthZ/access-control).

Rufen Sie zum Abrufen der Sicherheits Beschreibung für eine vorhandene DDE-Freigabe die [**nddebug**](nddegetsharesecurity.md) -Funktion auf. Sie können die Informationen bearbeiten und dann die Sicherheits Beschreibung für die Freigabe aktualisieren, indem Sie die [**nddesetsharesecurity**](nddesetsharesecurity.md) -Funktion verwenden.

 

 
