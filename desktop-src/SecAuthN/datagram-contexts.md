---
description: Die Semantik für Datagrammkontexte oder verbindungslose Kontexte unterscheidet sich geringfügig von denen für verbindungsorientierte Kontexte.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Datagrammkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cade151c77b9ceec037de57e08bcc3a90638ddeb56f27764d5ad2799abc523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008648"
---
# <a name="datagram-contexts"></a>Datagrammkontexte

Die Semantik für [*Datagrammkontexte*](/windows/desktop/SecGloss/d-gly)oder verbindungslose Kontexte unterscheidet sich geringfügig von denen für verbindungsorientierte Kontexte. Im verbindungslosen [*Kontext*](/windows/desktop/SecGloss/c-gly)eines Datagramms kann ein Server nicht bestimmen, wann der Client die Verbindung heruntergefahren oder anderweitig beendet hat. Anders ausgedrückt: Es wird keine Beendigungsbenachrichtigung von der Transportanwendung an den Server übergeben, wie dies in einem verbindungsorientierten Kontext der Fall wäre.

Um einen Datagrammkontext zu verwenden, legt ein Client das ISC \_ REQ \_ DATAGRAM-Flag in seinem Aufruf der [**InitializeSecurityContext (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) fest.

> [!IMPORTANT]
> Das [Microsoft Kerberos-Paket](microsoft-kerberos.md) unterstützt keine Datagrammkontexte im Benutzer-zu-Benutzer-Modus.

 

Um einige Modelle, insbesondere RPC im DCE-Stil, besser zu unterstützen, gelten die folgenden Regeln, wenn der Client einen Datagrammkontext verwendet:

-   Das [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) erzeugt beim ersten Aufruf von [**InitializeSecurityContext (Allgemein) kein Authentifizierungsblob (binary**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)large object). [](/windows/desktop/SecGloss/b-gly) Der Client kann jedoch den zurückgegebenen Sicherheitskontext in einem Aufruf der [**MakeSignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-makesignature) verwenden, um eine Signatur für eine Nachricht zu generieren.
-   Das Sicherheitspaket muss ermöglichen, dass der Kontext mehrmals neu eingerichtet wird, damit der Server die Verbindung ohne vorherige Ankündigung löschen kann. Dies bedeutet, dass alle Schlüssel, die in den Funktionen [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) verwendet werden, in einen konsistenten [*Zustand*](/windows/desktop/SecGloss/s-gly)zurückgesetzt werden können.
-   Das Sicherheitspaket ermöglicht dem Aufrufer das Angeben von Sequenzinformationen und stellt diese Sequenzinformationen auf empfängerseitiger Seite bereit. Dies gilt zusätzlich zu allen Sequenzinformationen, die vom Paket verwaltet werden.

Ein Sicherheitspaket legt das DATAGRAM-Flag SECPKG \_ FLAG \_ fest, um anzugeben, dass es die Datagrammsemantik unterstützt.

 

 
