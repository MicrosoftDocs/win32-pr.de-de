---
description: Clientkontextinitialisierung
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Clientkontextinitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c0f2912de57487c1f30fdac1ef40740553947b993ef6f5179a028625f132af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141183"
---
# <a name="client-context-initialization"></a>Clientkontextinitialisierung

Um eine sichere Verbindung herzustellen, erhält der Client ein ausgehendes [*Anmeldeinformationshandle,*](/windows/desktop/SecGloss/c-gly) bevor eine Authentifizierungsanforderung an den Server gesendet wird. Der Server erstellt einen Sicherheitskontext für den Client aus der Authentifizierungsanforderung. An der Einrichtung der Authentifizierung sind zwei clientseitige SSPI-Funktionen beteiligt:

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) ruft einen Verweis auf zuvor abgerufene [*Anmeldeinformationen*](/windows/desktop/SecGloss/c-gly)ab.
-   [**InitializeSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) erstellt die anfänglichen Sicherheitstoken für Authentifizierungsanforderungen.

Code für diesen Prozess finden Sie in der **GenClientContext-Funktion** unter [Verwenden von SSPI mit einem Windows Sockets Client.](using-sspi-with-a-windows-sockets-client.md)

Wenn ein Clientprogramm anmeldeinformationen zusätzlich zu seinen eigenen Anmeldeinformationen wie einem anderen Benutzernamen, Domänennamen und Kennwort verwenden muss, stellt es diese im [**AcquireCredentialsHandle-Aufruf**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) mit einer [**SEC \_ WINNT-AUTH \_ \_ IDENTITY-Struktur**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) bereit, die die zusätzlichen Anmeldeinformationen angibt. Weitere Informationen zu Anmeldeinformationsfunktionen finden Sie unter [Credential Management](authentication-functions.md).

> [!Note]  
> Der **Flags-Member** der [**SEC \_ WINNT \_ AUTH \_ IDENTITY-Struktur**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) kann auf SEC \_ WINNT \_ AUTH IDENTITY ANSI festgelegt \_ \_ werden, wenn Zeichenfolgen in der Struktur ASCI oder OEM sind. ANSI-Zeichenfolgen können mit dem **Flags-Member** der **SEC \_ WINNT \_ AUTH \_ IDENTITY-Struktur** verwendet werden, die auf SEC \_ WINNT AUTH IDENTITY UNICODE festgelegt \_ \_ \_ ist, wenn sie zum ersten Mal mithilfe der [**MultiByteToWideChar-Funktion**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) in [*Unicode*](/windows/desktop/SecGloss/u-gly) konvertiert werden.

 

Um den ersten Abschnitt der Authentifizierung zu initiieren, ruft der Client [**InitializeSecurityContext (Allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) auf, um ein anfängliches Sicherheitstoken abzurufen, das in einer Verbindungsanforderungsnachricht an den Server gesendet werden soll.

Der Client verwendet die im Ausgabepufferdeskriptor empfangenen Sicherheitstokeninformationen, um eine Nachricht zu generieren, die an den Server gesendet werden soll. Die Erstellung der Nachricht in Bezug auf die Platzierung verschiedener Puffer usw. ist Teil des [*Anwendungsprotokolls*](/windows/desktop/SecGloss/a-gly) und muss von beiden Parteien verstanden werden.

Der Client überprüft den Rückgabestatus von [**InitializeSecurityContext (Allgemein),**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) um festzustellen, ob die Authentifizierung in einem einzigen Aufruf abgeschlossen wird. Der Rückgabestatus SEC \_ I CONTINUE NEEDED gibt \_ \_ an, dass das Sicherheitsprotokoll mehrere Authentifizierungsmeldungen erfordert. Weitere Informationen zu Kontextfunktionen finden Sie unter [Kontextverwaltung.](authentication-functions.md)

 

 
