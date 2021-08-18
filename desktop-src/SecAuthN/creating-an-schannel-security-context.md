---
description: Erläutert das Einrichten eines Sicherheitskontexts, der die Kommunikation zwischen einem Client und einem Server schützt.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Erstellen eines Schannel-Sicherheitskontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7373d2ed4f8cc385a2245e6971f8233aad052930d4995225abfda8eab0191aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008858"
---
# <a name="creating-an-schannel-security-context"></a>Erstellen eines Schannel-Sicherheitskontexts

Zum Einrichten eines [*Sicherheitskontexts,*](/windows/desktop/SecGloss/s-gly) der die Kommunikation zwischen einem Client und einem Server schützt, müssen beide am folgenden Informationsaustauschprozess teilnehmen:

## <a name="client"></a>Client

1.  Der Client ruft die [**InitializeSecurityContext(General)-Funktion**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) auf.
2.  Schannel beginnt mit der Erstellung eines Sicherheitskontexts gemäß den Regeln des ausgewählten Sicherheitsprotokolls. Der Rückgabecode der Funktion gibt an, ob der Client die Funktion erneut aufrufen muss. [**InitializeSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) gibt möglicherweise ein Token zurück, das den Kontext darstellt.
3.  Wenn ein Token zurückgegeben wurde, sendet der Client es an den Server.
4.  Wenn [**InitializeSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) SEC \_ E OK \_ zurückgibt, wird der Client fertig. Wenn die Funktion SEC I CONTINUE NEEDED zurückgibt, muss der Client warten, bis der Server \_ ein Token an sie \_ \_ sendet. Wenn der Client über das Token vom Server verfügt, muss er die **InitializeSecurityContext (General)-Funktion erneut** [*aufrufen.*](/windows/desktop/SecGloss/c-gly) (Kehren Sie zu Schritt 2 zurück.)

## <a name="server"></a>Server

1.  Der Server wartet darauf, dass ein Client eine Nachricht sendet, die ein Sicherheitstoken enthält. Der Server übergibt das vom Client empfangene Token an die [**AcceptSecurityContext(General)-Funktion.**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
2.  Schannel baut auf dem teilweisen Sicherheitskontext auf, der durch das Token dargestellt wird. Schannel gibt ein Token an den Server und einen Rückgabecode zurück, der angibt, ob der Server die Funktion erneut aufrufen muss.
3.  Wenn ein Token zurückgegeben wurde, sendet der Server es an den Client.
4.  Wenn [**AcceptSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) SEC \_ E OK \_ zurückgibt, ist der Server fertig. Wenn die Funktion SEC I CONTINUE NEEDED zurückgibt, muss der Server warten, bis der Client \_ ein Token an sie \_ \_ sendet. Wenn der Server über das Token vom Client verfügt, muss er die **AcceptSecurityContext(General)-Funktion erneut** aufrufen. (Kehren Sie zu Schritt 2 zurück.)

Wenn eine der Funktionen einen anderen Wert als SEC E OK, SEC I CONTINUE NEEDED oder SEC E INCOMPLETE MESSAGE (siehe folgenden Absatz) zurückgibt, \_ \_ ist ein Fehler \_ \_ \_ \_ \_ \_ aufgetreten. Client und Server sollten die [**DeleteSecurityContext-Funktion**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) aufrufen, um den teilweise eingerichteten Sicherheitskontext zu löschen.

Ein Sonderfall, der die Client- und Serververarbeitung ändern kann, ist, wenn zu wenig oder zu viele Informationen von der anderen Partei an den Client oder Server gesendet werden. Bei zu wenig Informationen geben beide Funktionen SEC \_ E \_ INCOMPLETE MESSAGE \_ zurück. Informationen zum Erkennen und Behandeln unzureichender oder übermäßiger Informationen finden Sie unter Zusätzliche Puffer, die [von Schannel zurückgegeben werden.](extra-buffers-returned-by-schannel.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchführen der Authentifizierung mit Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Zuordnen von Zertifikaten](mapping-certificates.md)
</dt> <dt>

[Manuelles Überprüfen von Schannel-Anmeldeinformationen](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
