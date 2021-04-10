---
description: Client kontextinitialisierung
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Client kontextinitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615ce5c157371f1ebfec685d6227bd11a1d76531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131064"
---
# <a name="client-context-initialization"></a>Client kontextinitialisierung

Zum Herstellen einer sicheren Verbindung ruft der Client ein Handle für ausgehende [*Anmelde*](/windows/desktop/SecGloss/c-gly) Informationen ab, bevor eine Authentifizierungsanforderung an den Server gesendet wird. Der Server erstellt in der Authentifizierungsanforderung einen Sicherheitskontext für den Client. Es gibt zwei Client seitige SSPI-Funktionen, die an der Authentifizierungs Einrichtung beteiligt sind:

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) erhält einen Verweis auf zuvor [*erhaltene Anmelde Informationen.*](/windows/desktop/SecGloss/c-gly)
-   [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) erstellt die anfänglichen Authentifizierungs Anforderungs-Sicherheits Token.

Code für diesen Prozess kann in der **genclientcontext** -Funktion in verwendet werden, [indem SSPI mit einem Windows Sockets-Client verwendet](using-sspi-with-a-windows-sockets-client.md)wird.

Wenn ein Client Programm zusätzlich zu seinen eigenen Anmelde Informationen, wie z. b. einem anderen Benutzernamen, einem anderen Domänen Namen und einem Kennwort, Anmelde Informationen verwenden muss, werden diese im [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Befehl mit einer [**sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur, die die zusätzlichen Anmelde Informationen angibt, bereitgestellt. Weitere Informationen zu Anmelde Informationsfunktionen finden Sie unter [Verwaltung](authentication-functions.md)von Anmelde Informationen.

> [!Note]  
> Der **Flags** -Member der [**sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur kann auf sec \_ Winnt \_ auth Identity ANSI festgelegt werden, \_ \_ Wenn es sich bei den Zeichen folgen in der Struktur um ASCI oder OEM handelt. ANSI-Zeichen folgen können mit dem **Flags** -Member der **sec \_ Winnt \_ auth- \_ Identitäts** Struktur verwendet werden, die auf sec \_ Winnt \_ auth \_ Identity Unicode festgelegt ist, \_ Wenn Sie zunächst mithilfe der [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion in [*Unicode*](/windows/desktop/SecGloss/u-gly) konvertiert werden.

 

Um den ersten Teil der Authentifizierung zu initiieren, ruft der Client [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) auf, um ein erstes Sicherheits Token zu erhalten, das in einer Verbindungs Anforderungs Nachricht an den Server gesendet wird.

Der Client verwendet die Sicherheitstokeninformationen, die im Ausgabepuffer Deskriptor empfangen werden, um eine Nachricht zu generieren, die an den Server gesendet wird. Die Erstellung der Nachricht im Hinblick auf die Platzierung verschiedener Puffer und so weiter ist Teil des [*Anwendungs Protokolls*](/windows/desktop/SecGloss/a-gly) und muss von beiden Parteien verstanden werden.

Der Client überprüft den Rückgabestatus von [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , um zu überprüfen, ob die Authentifizierung in einem einzelnen-Befehl durchgeführt wird. Der Rückgabestatus "SEK \_ \_ ." \_ , der fortgesetzt wird, gibt an, dass das Sicherheitsprotokoll mehrere Authentifizierungs Nachrichten erfordert. Weitere Informationen zu Kontextfunktionen finden Sie unter [Context Management (Kontext Verwaltung](authentication-functions.md)).

 

 
