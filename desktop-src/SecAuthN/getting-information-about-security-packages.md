---
description: Wenn ein Client beginnt, wählt er ein Sicherheitspaket für seine Transaktionen mit einem Server aus und kontaktiert dann diesen Server. Ein Server wählt mindestens ein Sicherheitspaket aus und wartet auf eine Clientverbindung.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Abrufen von Informationen zu Sicherheitspaketen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626b5bf53ddc9ef20f0110dc7695a7245245604ca9e11baa3cbb50b2c1bd393f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883100"
---
# <a name="getting-information-about-security-packages"></a>Abrufen von Informationen zu Sicherheitspaketen

Wenn ein Client beginnt, wählt [](/windows/desktop/SecGloss/s-gly) er ein Sicherheitspaket für seine Transaktionen mit einem Server aus und kontaktiert dann diesen Server. Ein Server wählt mindestens ein Sicherheitspaket aus und wartet auf eine Clientverbindung.

Für spezifische Informationen zu den SSPI-Sicherheitspaketen, die für einen bestimmten SSP verfügbar sind, kann die [**EnumerateSecurityPackages-Funktion**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) aufgerufen werden, um eine [**SecPkgInfo-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) abzurufen.

Um die Ausgabestruktur abzurufen, übergibt der Aufrufer die Adresse eines Zeigers auf den Typ der Rückgabestruktur an die Funktion. Die Funktion weist Arbeitsspeicher zu und gibt die Daten an den Aufrufer zurück, indem dem Argument die Adresse des Rückgabedatenpuffers zugewiesen wird. Die SSPI-Konvention ist, dass die Funktion Speicher für die Struktur zuordnt, und die aufrufende Anwendung gibt diesen Arbeitsspeicher mithilfe von [**FreeContextBuffer frei.**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer)

Durch Aufrufen [**der QuerySecurityPackageInfo-Funktion**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) werden die Attribute eines [*Sicherheitspakets abgerufen.*](/windows/desktop/SecGloss/s-gly) Sowohl der Server als auch der Client können die **QuerySecurityPackageInfo-Funktion** aufrufen, um die maximale Länge des Sicherheitstokens vom **cbMaxToken-Member** der [**SecPkgInfo-Struktur abzurufen.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) Ein Beispiel finden Sie im Aufruf der **QuerySecurityPackageInfo-Funktion** unter Verwenden von SSPI mit einem Windows [Sockets Server.](using-sspi-with-a-windows-sockets-server.md)

Weitere Informationen zu Paketfunktionen finden Sie unter [Paketverwaltung](authentication-functions.md).

 

 
