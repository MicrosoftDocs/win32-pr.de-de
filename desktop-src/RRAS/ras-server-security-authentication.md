---
title: RAS-Serversicherheitsauthentifizierung
description: Wenn ein Windows NT/Windows 2000 RAS-Server einen Aufruf empfängt, ruft er die RasSecurityDialogBegin-Funktion der registrierten RAS-Sicherheits-DLL auf, sofern vorhanden.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532bda51d6e9ee0ea90c900fa974827e1840e7e633caf48fbadec5fe6a701a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028740"
---
# <a name="ras-server-security-authentication"></a>RAS-Serversicherheitsauthentifizierung

Wenn ein Windows NT/Windows 2000 RAS-Server einen Aufruf empfängt, ruft er die [**RasSecurityDialogBegin-Funktion**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) der registrierten RAS-Sicherheits-DLL auf, sofern vorhanden. Dieser Aufruf benachrichtigt die Sicherheits-DLL, mit der Authentifizierung des Remotebenutzers zu beginnen. Der RAS-Server ruft **RasSecurityDialogBegin** auf, bevor er die ZUGEHÖRIGE ODER RAS-Authentifizierung ausführt.

Der [**RasSecurityDialogBegin-Aufruf**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) übergibt die folgenden Informationen an die Sicherheits-DLL:

-   Ein Porthandle zum Identifizieren der Verbindung.
-   Zeiger auf Puffer, die bei der Kommunikation mit dem Remotebenutzer verwendet werden sollen.
-   Ein Zeiger auf eine [**RasSecurityDialogComplete-Funktion,**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) die aufgerufen werden soll, wenn die Authentifizierung abgeschlossen ist.

Porthandle und Pufferzeiger sind gültig, bis die Sicherheits-DLL [**RasSecurityDialogComplete aufruft,**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) um die Authentifizierungstransaktion zu beenden.

[**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) benachrichtigt den RAS-Server über die Ergebnisse der Authentifizierung des Remotebenutzers durch die Sicherheits-DLL. Wenn die Sicherheits-DLL erfolglos meldet, fährt der RAS-Server mit seiner MSI- und RAS-Authentifizierung des Remotebenutzers fort. Wenn die Sicherheits-DLL meldet, dass der Remotebenutzer die Authentifizierung nicht bestanden hat oder dass ein Fehler aufgetreten ist, hängt der RAS-Server auf und protokolliert den Fehler oder die fehlgeschlagene Authentifizierung im Ereignisprotokoll.

 

 




