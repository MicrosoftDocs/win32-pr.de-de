---
title: RAS-Sicherheits-DLL-Authentifizierungs Transaktion
description: Der Windows NT-/Windows 2000-RAS-Server Ruft die Funktion "rassecuritydialogbegin" der Sicherheits-DLL auf, um die Authentifizierung eines Remote Benutzers zu starten.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109f6ad5cd3d7b76e30db099a478ffaf562feb32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517042"
---
# <a name="ras-security-dll-authentication-transaction"></a>RAS-Sicherheits-DLL-Authentifizierungs Transaktion

Der Windows NT-/Windows 2000-RAS-Server Ruft die Funktion " [**rassecuritydialogbegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) " der Sicherheits-DLL auf, um die Authentifizierung eines Remote Benutzers zu starten. Der RAS-Server ist blockiert und kann keine anderen Aufrufe akzeptieren, bis " **rassecuritydialogbegin** " zurückgegeben wird. Aus diesem Grund sollte " **rassecuritydialogbegin** " die Eingabeparameter kopieren, einen Thread zum Ausführen der Authentifizierung erstellen und so schnell wie möglich zurückgeben.

Der von der Sicherheits-DLL erstellte Thread verwendet die Funktionen " [**rassecuritydialogsend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) " und " [**rassecuritydialogreceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) ", um mit dem Remote Computer zu kommunizieren. Diese Funktionen sind für den statischen Import aus einer Bibliothek nicht verfügbar. Stattdessen muss die Sicherheits-DLL die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit diesen Funktionen in RASMAN.DLL zu verknüpfen.

Während einer Authentifizierungs Transaktion zeigt der RAS-Verbindungs-Manager auf dem Remote Computer ein Terminalfenster an. Der Thread der Sicherheits-DLL ruft " [**rassecuritydialogsend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) " auf, um eine Nachricht zu senden, die im Terminalfenster angezeigt werden soll. Der Thread ruft dann " [**rassecuritydialogreceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) " auf, um die Eingabe zu empfangen, die der Remote Benutzer im Terminalfenster eingibt. Der Thread kann eine beliebige Anzahl von " **rassecuritydialogsend** "-aufrufen ausführen, gefolgt von einem " **rassecuritydialogreceive** "-Aufruf. Nach jedem Aufrufe von " **rassecuritydialogreceive**" muss der Thread eine der Wait-Funktionen, z. b. " [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)", abrufen, um zu warten, bis die asynchronen Sende-und Empfangs Vorgänge abgeschlossen sind. Der RAS-Server signalisiert einem Ereignis Objekt, wenn der Empfangsvorgang abgeschlossen wurde oder wenn ein optionales Timeout Intervall verstrichen ist.

Wenn die Authentifizierung des Remote Benutzers durch den Thread abgeschlossen ist, wird die Funktion " [**rassecuritydialogcomplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) " aufgerufen. Dieser Befehl übergibt eine [**Sicherheits \_ Nachrichten**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) Struktur, die die Ergebnisse der Authentifizierungs Transaktion enthält, an den RAS-Server. Der RAS-Server führt dann eine cleanupsequenz aus, die einen aufzurufenden Befehl der " [**rassecuritydialogend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) "-Funktion der dll enthält. Dadurch erhält die Sicherheits-DLL die Möglichkeit, alle notwendigen Bereinigungs Vorgänge auszuführen.

Die Sicherheits-DLL kann die Funktion " [**rassecuritydialoggetinfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) " aufrufen, um Informationen über den Port abzurufen, der einer Authentifizierungs Transaktion zugeordnet ist. **Rassecuritydialoggetinfo** füllt eine [**RAS- \_ Sicherheits \_ Informations**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) Struktur aus, die den Status des letzten " [**rassecuritydialogreceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) "-Aufrufens für den Port angibt.

 

 