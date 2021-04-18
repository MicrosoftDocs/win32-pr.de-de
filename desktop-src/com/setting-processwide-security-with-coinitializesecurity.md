---
title: Festlegen der Process-Wide Sicherheit mit CoInitializeSecurity
description: Mit der CoInitializeSecurity-Funktion können Sie komplexe Sicherheitsszenarien steuern, indem Sie die Sicherheit für eine Anwendung Programm gesteuert festlegen.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567a6dfaf47dbd278fc248558cd25969c733b24a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391076"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Festlegen der Process-Wide Sicherheit mit CoInitializeSecurity

Mit der [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion können Sie komplexe Sicherheitsszenarien steuern, indem Sie die Sicherheit für eine Anwendung Programm gesteuert festlegen. In diesem Thema werden Szenarien beschrieben, in denen **CoInitializeSecurity** verwendet werden kann, und es werden einige Details zur Verwendung beschrieben.

Es gibt mehrere Gründe, warum Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) verwenden möchten, um die Prozess weite Sicherheit innerhalb des Programms festzulegen. Obwohl Sie die Authentifizierungs Ebene und die Zugriffsberechtigungen für die Anwendung mithilfe von dcomcnfg.exe festlegen können, ist die standardmäßige Identitätswechsel Ebene für den Computer möglicherweise nicht die für den Prozess gewünschte. Die einzige Möglichkeit, diese Einstellung für Ihren Prozess zu ändern, besteht darin, **CoInitializeSecurity** aufzurufen.

Wenn Sie den SChannel-Sicherheitsanbieter verwenden möchten, müssen Sie ihn in einem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf als Authentifizierungsdienst angeben.

Ein weiteres häufiges Szenario, in dem Sie die Prozess weite Sicherheit Programm gesteuert festlegen können, ist, wenn Sie die Standard Sicherheit für den gesamten Prozess festlegen möchten, aber über ein oder mehrere Objekte innerhalb dieses Prozesses verfügen, die Schnittstellen mit speziellen Sicherheitsanforderungen verfügbar machen. In diesem Fall können Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) so einrichten, dass die Sicherheit für den Prozess festgelegt wird, sodass com den größten Teil der Sicherheitsüberprüfungen ermöglicht und andere Methoden aufgerufen werden können, um die Sicherheit für die Objekte mit speziellen Sicherheitsanforderungen festzulegen. Das Aufrufen dieser Methoden und Funktionen wird unter [Festlegen der Sicherheit auf der Ebene der Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md)beschrieben.

Wenn Ihre Anwendung über sehr spezielle Sicherheitsanforderungen verfügt, z. b. das zulassen, dass bestimmte Gruppen Zugriff auf verschiedene Objekte haben, hängt von der Tageszeit ab, sollten Sie die gesamte Sicherheit Programm gesteuert verarbeiten und sicherstellen, dass com keinerlei automatische Überprüfung durchführt. Zu diesem Zweck müssen Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen und den *dwauthnlevel* -Parameter auf None und den *pVoid* -Parameter auf **null** festlegen. Wenn Sie über ein eigenes Sicherheitspaket verfügen, müssen Sie es auch im *pauthnsvc* -Parameter registrieren. Anschließend können Sie die gesamte eigene Sicherheit Programm gesteuert über Aufrufe der Proxy-Level-Schnittstelle und der Funktionen verarbeiten, [die unter Festlegen der Sicherheit auf der Schnittstellen Proxy Ebene](setting-security-at-the-interface-proxy-level.md)beschrieben werden.

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) bietet einen umfangreichen Satz an Funktionen. Wenn Sie **CoInitializeSecurity** aufzurufen, werden die Registrierungs Werte ignoriert, und die an den-Befehl übergebenen sicherheitsinitialisierungs Werte werden stattdessen verwendet. Abhängig vom gewünschten Ergebnis kann der erste Parameter ( *pVoid*) auf drei verschiedene Werttypen verweisen: eine [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , ein [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) -Objekt oder ein Zeiger auf eine AppID. In den meisten Fällen verwenden Sie Windows-Funktionen, um eine **Sicherheits \_ Beschreibung** zu erstellen, auf die *pVoid* verweist.

*PVoid* kann jedoch auch auf ein [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) -Objekt verweisen.

Um [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) anzugeben, dass Sie ein [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) -Objekt an *pVoid* übergeben, müssen Sie den Wert der eoac- \_ Zugriffs \_ Steuerung an den *dwfunktionen* -Parameter übergeben. Da **CoInitializeSecurity** die Ergebnisse von Zugriffs Überprüfungen zwischenspeichert, darf die Zugriffs Steuerungs Liste nach dem Aufrufen von **CoInitializeSecurity** nicht geändert werden.

Ein anderer Typ von Wert, den Sie an den *pVoid* -Parameter übergeben können, ist ein Zeiger auf eine GUID, die die AppID der Anwendung ist. Wenn *pVoid* ein Zeiger auf eine AppID ist, müssen Sie die eoac- \_ AppID im *pFunctions* -Parameter angeben, damit die Funktion weiß, welcher Wert in *pVoid* zu erwarten ist. Wenn *pVoid* auf eine AppID verweist, verwendet [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nur die Registrierung für Authentifizierungs Werte und ignoriert alle anderen Parameter für **CoInitializeSecurity**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen Process-Wide Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 