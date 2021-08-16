---
title: RAS-Sicherheits-DLL-Authentifizierungstransaktion
description: Windows NT/Windows 2000 RAS-Server ruft die RasSecurityDialogBegin-Funktion der Sicherheits-DLL auf, um eine Authentifizierung eines Remotebenutzers zu starten.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea463c56d96cad13fb55a2b6e0bbdfc154518ba012e4c71c6ab8bdd3213cd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789476"
---
# <a name="ras-security-dll-authentication-transaction"></a>RAS-Sicherheits-DLL-Authentifizierungstransaktion

Windows NT/Windows 2000 RAS-Server ruft die [**RasSecurityDialogBegin-Funktion**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) der Sicherheits-DLL auf, um eine Authentifizierung eines Remotebenutzers zu starten. Der RAS-Server ist blockiert und kann keine weiteren Aufrufe akzeptieren, bis **RasSecurityDialogBegin** zurückgegeben wird. Aus diesem Grund sollte **RasSecurityDialogBegin** die Eingabeparameter kopieren, einen Thread zum Durchführen der Authentifizierung erstellen und so schnell wie möglich zurückgeben.

Der von der Sicherheits-DLL erstellte Thread verwendet die Funktionen [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) und [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) für die Kommunikation mit dem Remotecomputer. Diese Funktionen sind für den statischen Import aus keiner Bibliothek verfügbar. Stattdessen muss die Sicherheits-DLL die Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit diesen Funktionen in RASMAN.DLL zu verknüpfen.

Während einer Authentifizierungstransaktion zeigt der RAS-Verbindungs-Manager auf dem Remotecomputer ein Terminalfenster an. Der Thread der Sicherheits-DLL ruft [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) auf, um eine Meldung zu senden, die im Terminalfenster angezeigt werden soll. Der Thread ruft dann [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) auf, um die Eingabe zu erhalten, die der Remotebenutzer im Terminalfenster eingibt. Der Thread kann eine beliebige Anzahl von **RasSecurityDialogSend-Aufrufen** mit jedem Aufruf gefolgt von einem **RasSecurityDialogReceive-Aufruf** vornehmen. Nach jedem Aufruf von **RasSecurityDialogReceive** muss der Thread eine der Wartefunktionen wie [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)aufrufen, um auf den Abschluss der asynchronen Sende- und Empfangsvorgänge zu warten. Der RAS-Server signalisiert ein Ereignisobjekt, wenn der Empfangsvorgang abgeschlossen wurde oder ein optionales Time out-Intervall verstrichen ist.

Wenn der Thread die Authentifizierung des Remotebenutzers abgeschlossen hat, ruft er die [**RasSecurityDialogComplete-Funktion auf.**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) Dieser Aufruf übergibt eine [**SECURITY \_ MESSAGE-Struktur,**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) die die Ergebnisse der Authentifizierungstransaktion enthält, an den RAS-Server. Der RAS-Server führt dann eine Bereinigungssequenz aus, die einen Aufruf der [**RasSecurityDialogEnd-Funktion**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) der DLL enthält. Dies gibt der Sicherheits-DLL die Möglichkeit, alle erforderlichen Bereinigungen durchzuführen.

Die Sicherheits-DLL kann die [**RasSecurityDialogGetInfo-Funktion**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) aufrufen, um Informationen über den Port abzurufen, der einer Authentifizierungstransaktion zugeordnet ist. **RasSecurityDialogGetInfo** füllt eine [**RAS SECURITY \_ \_ INFO-Struktur**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) aus, die den Status des letzten [**RasSecurityDialogReceive-Aufrufs**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) für den Port angibt.

 

 