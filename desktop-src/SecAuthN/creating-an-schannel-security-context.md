---
description: Erläutert das Einrichten eines Sicherheits Kontexts, der die Kommunikation zwischen einem Client und einem Server schützt.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Erstellen eines SChannel-Sicherheits Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348004"
---
# <a name="creating-an-schannel-security-context"></a>Erstellen eines SChannel-Sicherheits Kontexts

Zum Einrichten eines [*Sicherheits Kontexts*](/windows/desktop/SecGloss/s-gly) , der die Kommunikation zwischen einem Client und einem Server schützt, müssen beide am folgenden Informationsaustausch Prozess teilnehmen:

## <a name="client"></a>Client

1.  Der Client ruft die [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion auf.
2.  SChannel beginnt mit dem Erstellen eines Sicherheits Kontexts gemäß den Regeln des ausgewählten Sicherheitsprotokolls. Der Rückgabecode der Funktion gibt an, ob die Funktion vom Client erneut aufgerufen werden muss. [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) gibt möglicherweise ein Token zurück, das den Kontext darstellt.
3.  Wenn ein Token zurückgegeben wurde, sendet der Client es an den Server.
4.  Wenn [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sec \_ E OK zurückgibt \_ , ist der Client abgeschlossen. Wenn die Funktion Sekunde zurück \_ gibt \_ , die ich weiterhin \_ benötigtes, muss der Client warten, bis der Server ihm ein Token sendet. Wenn der Client über das Token vom Server verfügt, muss die [*Funktion*](/windows/desktop/SecGloss/c-gly) **InitializeSecurityContext (General)** erneut aufgerufen werden. (Kehren Sie zu Schritt 2 zurück.)

## <a name="server"></a>Server

1.  Der Server wartet darauf, dass ein Client eine Nachricht sendet, die ein Sicherheits Token enthält. Der Server übergibt das vom Client empfangene Token an die Funktion " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) ".
2.  SChannel baut auf dem partiellen Sicherheitskontext auf, der durch das Token dargestellt wird. SChannel gibt ein Token an den Server zurück, und einen Rückgabecode, der angibt, ob der Server die Funktion erneut abrufen muss.
3.  Wenn ein Token zurückgegeben wurde, sendet der Server es an den Client.
4.  Wenn " [**Accept-SecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) " sec \_ E OK zurückgibt, erfolgt \_ der Server. Wenn die Funktion "s" zurückgibt \_ , die ich \_ weiterhin \_ benötigtes, muss der Server warten, bis der Client ihm ein Token sendet. Wenn der Server über das Token des Clients verfügt, muss er die Funktion " **Accept tsecuritycontext (General)** " erneut abrufen. (Kehren Sie zu Schritt 2 zurück.)

Wenn eine der beiden Funktionen einen anderen Wert als s OK zurückgibt \_ \_ , ist der Vorgang \_ \_ weiterhin \_ erforderlich, oder \_ \_ \_ es ist keine unvollständige Nachricht (siehe folgender Absatz) aufgetreten. Der Client und der Server sollten die [**Delta Context**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) -Funktion zum Löschen des teilweise eingerichteten Sicherheits Kontexts abrufen.

Ein Sonderfall, der die Client-und Server Verarbeitung ändern kann, liegt vor, wenn zu wenig oder zu viele Informationen von der anderen Partei an den Client oder Server gesendet werden. Wenn zu wenig Informationen angezeigt werden, geben beide Funktionen eine nicht abgeschlossene Sekunde in Sekunden zurück \_ \_ \_ . Informationen zum erkennen und behandeln unzureichender oder übermäßiger Informationen finden Sie unter [von SChannel zurückgegebene zusätzliche Puffer](extra-buffers-returned-by-schannel.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchführen der Authentifizierung mithilfe von SChannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Zuordnung von Zertifikaten](mapping-certificates.md)
</dt> <dt>

[Manuelles Überprüfen von SChannel-Anmelde Informationen](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
