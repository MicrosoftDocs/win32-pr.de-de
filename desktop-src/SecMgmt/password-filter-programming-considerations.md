---
description: Erläutert Überlegungen zur Implementierung von Exportfunktionen für Kennwortfilter.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Überlegungen zur Programmierung von Kennwortfiltern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9270a08c51b4b3e6b07923ad9461dc2e2dd418c3be1f1a181c07f940d71ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005088"
---
# <a name="password-filter-programming-considerations"></a>Überlegungen zur Programmierung von Kennwortfiltern

Beachten Sie beim Implementieren von Exportfunktionen für [*Kennwortfilter*](/windows/desktop/SecGloss/p-gly) die folgenden Überlegungen:

-   Achten Sie bei der Arbeit mit [*Klartext-Kennwörtern*](/windows/desktop/SecGloss/p-gly) auf Vorsicht. Das Senden von Klartext-Kennwörtern über Netzwerke kann die Sicherheit gefährden. Netzwerk-"Sniffers" können problemlos auf Klartext-Kennwortdatenverkehr achten.
-   Löschen Sie den gesamten Arbeitsspeicher, der zum Speichern von Kennwörtern verwendet wird, indem Sie die [**SecureZeroMemory-Funktion**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) aufrufen, bevor Sie Arbeitsspeicher freigeben.
-   Alle Puffer, die an Kennwortbenachrichtigungs- und Filterroutinen übergeben werden, sollten als schreibgeschützt behandelt werden. Das Schreiben von Daten in diese Puffer kann zu instabilem Verhalten führen.
-   Alle Kennwortbenachrichtigungs- und Filterroutinen sollten threadsicher sein. Verwenden Sie kritische Abschnitte oder andere synchrone Programmiertechniken, um Daten nach Bedarf zu schützen.
-   Kennwortbenachrichtigungen und Filterung erfolgen nur auf dem Computer, auf dem sich das Konto befindet.
-   Da alle Domänencontroller schreibbar sind, müssen Kennwortfilterpakete auf allen Domänencontrollern vorhanden sein.

    **Windows NT 4.0-Domänen:** Benachrichtigungen zu Domänenkonten erfolgen nur auf dem primären Domänencontroller. Zusätzlich zum primären Domänencontroller sollten die Kennwortfilterpakete auf allen Sicherungsdomänencontrollern installiert werden, damit Benachrichtigungen bei Änderungen der Serverrolle fortgesetzt werden können.

-   Alle Kennwortfilter-DLLs werden im [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) des lokalen Systemkontos ausgeführt.



| Informationen über                                                                                                                     | Finden Sie unter                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Installieren und Registrieren Einer eigenen [*Kennwortfilter-DLL*](/windows/desktop/SecGloss/p-gly) | [Installieren und Registrieren einer Kennwortfilter-DLL](installing-and-registering-a-password-filter-dll.md) |
| Die von Microsoft bereitgestellte Kennwortfilter-DLL.                                                                                            | [Erzwingung und Passfilt.dllvon sicheren Kennwörtern ](strong-password-enforcement-and-passfilt-dll.md)         |
| Exportieren von Funktionen, die von einer Kennwortfilter-DLL implementiert werden.                                                                                    | [Kennwortfilterfunktionen](management-functions.md)                          |



 

 

 
