---
title: Bestimmen Ihrer Sicherheitsanforderungen
description: Wie Sie die com-Sicherheit für Ihre Anwendung einrichten, hängt von der Art der Sicherheit ab, die Ihre Anwendung benötigt. Es gibt verschiedene häufige Situationen, die bestimmen, was Sie tun sollten.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714435"
---
# <a name="determining-your-security-needs"></a>Bestimmen Ihrer Sicherheitsanforderungen

Wie Sie die com-Sicherheit für Ihre Anwendung einrichten, hängt von der Art der Sicherheit ab, die Ihre Anwendung benötigt. Es gibt verschiedene häufige Situationen, die bestimmen, was Sie tun sollten.

Wenn Sie sich dafür entscheiden, die com-Sicherheits Standardwerte zu verwenden, müssen Sie den com-Vorgang nicht alle durchführen. Informationen dazu, was diese Standardeinstellungen sind, finden Sie unter [com-Sicherheits Standardwerte](com-security-defaults.md).

Sie können auch Remote Aufrufe an Ihren Computer verhindern, indem Sie DCOM vollständig deaktivieren (com zwischen Remote Computern). Weitere Informationen finden Sie unter [Festlegen von System-Wide Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Für ältere oder neue Anwendungen können Sie die Prozess weite Sicherheit in der Registrierung festlegen. Weitere Informationen finden Sie unter [Festlegen von Processwide Security über die Registrierung](setting-processwide-security-through-the-registry.md).

Sie können auch die Standard Sicherheitseinstellungen für Aufrufe bestimmter Schnittstellen im Prozess überschreiben, während Sie die Standard Sicherheit für den Rest des Prozesses festlegen (damit com die allgemeinen Fälle verarbeiten kann). Weitere Informationen finden Sie unter [Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md).

Um komplexe Sicherheitsanforderungen zu erfüllen, können Sie die gesamte Sicherheit Programm gesteuert verarbeiten, anstatt com die Handhabung für Sie zu erlauben. Dazu wird [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen, um die automatische Authentifizierung zu deaktivieren, und dann alle Sicherheitseinstellungen zu steuern, indem die Sicherheit für einen Proxy pro Schnittstelle festgelegt wird. Weitere Informationen finden Sie unter [Festlegen von Processwide Security mit CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) und [Festlegen der Sicherheit auf der Ebene der Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md).

In einigen Szenarien sollten Sie die Sicherheit vollständig deaktivieren. Sie können entscheiden, dass Ihre Anwendung keine Sicherheit benötigt, oder Sie können die Sicherheit während der Entwicklungszeit deaktivieren, damit Sie die Sicherheitsfeatures einzeln aktivieren können. Informationen zum Deaktivieren der com-Sicherheit finden Sie unter [Ausschalten der Sicherheit](turning-off-security.md).

Die Sicherheit in com basiert auf Authentifizierungsdiensten, die von Sicherheitspaketen verwaltet werden. NTLMSSP funktioniert für viele Anwendungen gut, bietet jedoch nicht die stabilere Sicherheit, die von anderen Paketen geboten wird. Daher unterstützt com das SChannel-Sicherheitspaket und das Kerberos V5-Sicherheitsprotokoll. Weitere Informationen zur Verwendung dieser Sicherheitspakete finden Sie unter [com-und Sicherheitspakete](com-and-security-packages.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




