---
description: Wenn ein Client beginnt, wählt er ein Sicherheitspaket für seine Transaktionen mit einem Server aus und kontaktiert dann den Server. Ein Server wählt mindestens ein Sicherheitspaket aus und wartet auf eine Client Verbindung.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Informationen zu Sicherheitspaketen erhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129924"
---
# <a name="getting-information-about-security-packages"></a>Informationen zu Sicherheitspaketen erhalten

Wenn ein Client beginnt, wählt er ein [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) für seine Transaktionen mit einem Server aus und kontaktiert dann den Server. Ein Server wählt mindestens ein Sicherheitspaket aus und wartet auf eine Client Verbindung.

Für spezifische Informationen zu den SSPI-Sicherheitspaketen, die mit einem bestimmten SSP verfügbar sind, kann die [**enumeratesecuritypackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) -Funktion aufgerufen werden, um eine [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur abzurufen.

Zum Abrufen der Ausgabestruktur übergibt der Aufrufer die Adresse eines Zeigers auf den Typ der Rückgabe Struktur an die Funktion. Die-Funktion ordnet Speicher zu und gibt die Daten an den Aufrufer zurück, indem die Adresse des Rückgabe Daten Puffers dem-Argument zugewiesen wird. Die SSPI-Konvention ist, dass die Funktion Arbeitsspeicher für die Struktur zuweist, und die aufrufenden Anwendung gibt diesen Speicher mit [**freecontextbuffer frei**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).

Durch Aufrufen der [**querysecuritypackageinfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) -Funktion werden die Attribute eines [*Sicherheitspakets*](/windows/desktop/SecGloss/s-gly)abgerufen. Sowohl der Server als auch der Client können die **querysecuritypackageinfo** -Funktion aufgerufen werden, um die maximale Länge des Sicherheits Tokens vom **cbmaxtoken** -Member der [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur abzurufen. Ein Beispiel finden Sie unter Verwenden der Funktion " **querysecuritypackageinfo** ", die in [Verwenden von SSPI mit einem Windows Sockets-Server](using-sspi-with-a-windows-sockets-server.md)gezeigt wird.

Weitere Informationen zu Paketfunktionen finden Sie unter [Paketverwaltung](authentication-functions.md).

 

 
