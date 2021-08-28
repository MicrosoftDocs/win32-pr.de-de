---
title: Festlegen Process-Wide Sicherheit mit CoInitializeSecurity
description: Mit der CoInitializeSecurity-Funktion können Sie komplexe Sicherheitsszenarien steuern, indem Sie die Sicherheit für eine Anwendung programmgesteuert festlegen.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c3e601897e9f2313682a3474c1760bc211285d8fa81a82f67d114681a7a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610890"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Festlegen Process-Wide Sicherheit mit CoInitializeSecurity

Mit [**der CoInitializeSecurity-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) können Sie komplexe Sicherheitsszenarien steuern, indem Sie die Sicherheit für eine Anwendung programmgesteuert festlegen. Dieses Thema beschreibt Szenarien, in denen Sie **CoInitializeSecurity** verwenden können, und enthält einige Details zur Verwendung.

Es gibt mehrere Gründe, warum Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) verwenden möchten, um die prozessweite Sicherheit in Ihrem Programm festzulegen. Obwohl Sie beispielsweise die Authentifizierungsebene und die Zugriffsberechtigungen für die Anwendung mithilfe von dcomcnfg.exe festlegen können, ist die Standardidentitätswechselebene für den Computer möglicherweise nicht die für Ihren Prozess gewünschte Ebene. Die einzige Möglichkeit, diese Einstellung für Ihren Prozess zu ändern, besteht darin, **CoInitializeSecurity** aufzurufen.

Wenn Sie den Schannel-Sicherheitsanbieter verwenden möchten, müssen Sie ihn in einem Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)als Authentifizierungsdienst angeben.

Ein weiteres häufiges Szenario, in dem Sie die prozessweite Sicherheit programmgesteuert festlegen können, ist, wenn Sie die Standardsicherheit für den gesamten Prozess festlegen möchten, aber über ein oder mehrere Objekte innerhalb dieses Prozesses verfügen, die Schnittstellen mit besonderen Sicherheitsanforderungen verfügbar machen. In diesem Fall können Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, um die Sicherheit für den Prozess festzulegen, sodass COM die meisten Sicherheitsüberprüfungen verarbeiten kann, und Sie können andere Methoden aufrufen, um die Sicherheit für die Objekte mit besonderen Sicherheitsanforderungen festzulegen. Das Aufrufen dieser Methoden und Funktionen wird unter [Festlegen der Sicherheit auf Schnittstellenproxyebene](setting-security-at-the-interface-proxy-level.md)beschrieben.

Wenn Ihre Anwendung sehr spezielle Sicherheitsanforderungen hat, z. B. bestimmten Gruppen den Zugriff auf verschiedene Objekte je nach Tageszeit zulässt, sollten Sie die gesamte Sicherheit programmgesteuert behandeln und sicherstellen, dass COM keine automatische Überprüfung für Sie vorliegt. Hierzu müssen Sie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen und den *dwAuthnLevel-Parameter* auf none und den *pVoid-Parameter* auf **NULL** festlegen. Wenn Sie über ein eigenes Sicherheitspaket verfügen, müssen Sie es auch im *pAuthnSvc-Parameter* registrieren. Anschließend können Sie ihre gesamte Sicherheit programmgesteuert durch Aufrufe der Schnittstelle auf Proxyebene und der funktionen behandeln, die unter Festlegen der [Sicherheit auf Schnittstellenproxyebene](setting-security-at-the-interface-proxy-level.md)beschrieben werden.

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) bietet eine Vielzahl von Funktionen. Wenn Sie **CoInitializeSecurity** aufrufen, werden die Registrierungswerte ignoriert, und die Sicherheitsinitialisierungswerte, die Sie an den Aufruf übergeben, werden stattdessen verwendet. Je nach gewünschtem Ergebnis kann der erste Parameter *pVoid* auf drei verschiedene Typen von Werten verweisen: einen [**SECURITY \_ DESCRIPTOR,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) ein [**IAccessControl-Objekt**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) oder einen Zeiger auf eine AppID. In den meisten Fällen verwenden Sie Windows Funktionen, um einen **\_ SICHERHEITSDESKRIPTOR** zu erstellen, auf den *pVoid* verweist.

*pVoid* kann jedoch auch auf ein [**IAccessControl-Objekt**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) verweisen.

Um [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) anzugeben, dass Sie ein [**IAccessControl-Objekt**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) an *pVoid* übergeben, müssen Sie den \_ EOAC ACCESS \_ CONTROL-Wert an den *dwCapabilities-Parameter* übergeben. Da **CoInitializeSecurity** die Ergebnisse der Zugriffsüberprüfungen zwischenspeichert, darf die Zugriffssteuerungsliste nach dem Aufruf von **CoInitializeSecurity** nicht geändert werden.

Ein anderer Werttyp, den Sie an den *pVoid-Parameter* übergeben können, ist ein Zeiger auf eine GUID, d.h. die AppID Ihrer Anwendung. Wenn *pVoid* ein Zeiger auf eine AppID ist, müssen Sie \_ EOAC APPID im *pCapabilities-Parameter* angeben, damit die Funktion weiß, welcher Wert in *pVoid* zu erwarten ist. Wenn *pVoid* auf eine AppID verweist, verwendet [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nur die Registrierung für Authentifizierungswerte und ignoriert alle anderen Parameter für **CoInitializeSecurity.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Process-Wide Security](setting-processwide-security.md)
</dt> </dl>

 

 