---
title: Ermitteln Ihrer Sicherheitsanforderungen
description: Wie Sie die COM-Sicherheit für Ihre Anwendung einrichten, hängt davon ab, welche Art von Sicherheit Ihre Anwendung benötigt. Es gibt mehrere häufige Situationen, die bestimmen, was Sie tun sollten.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57ccbbc8fc96b7c94e90fd3925dfb2ffff07225c34ebe1da34353f42b08b3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993230"
---
# <a name="determining-your-security-needs"></a>Ermitteln Ihrer Sicherheitsanforderungen

Wie Sie die COM-Sicherheit für Ihre Anwendung einrichten, hängt davon ab, welche Art von Sicherheit Ihre Anwendung benötigt. Es gibt mehrere häufige Situationen, die bestimmen, was Sie tun sollten.

Wenn Sie sich für die Verwendung der COM-Sicherheitsstandards entscheiden, müssen Sie nichts unternehmen– "COM übernimmt alles." Informationen zu diesen Standardeinstellungen finden Sie unter [COM-Sicherheitsstandards.](com-security-defaults.md)

Sie können auch Remoteaufrufe an Ihren Computer verhindern, indem Sie DCOM vollständig deaktivieren (COM zwischen Remotecomputern). Weitere Informationen finden Sie unter [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Für ältere oder neue Anwendungen können Sie die prozessweite Sicherheit in der Registrierung festlegen. Weitere Informationen finden Sie unter [Festlegen der prozessweiten Sicherheit über die Registrierung.](setting-processwide-security-through-the-registry.md)

Sie können auch Standardsicherheitseinstellungen für Aufrufe bestimmter Schnittstellen im Prozess außer Kraft setzen, während Sie die Standardsicherheit für den Rest des Prozesses festlegen (damit COM die allgemeinen Fälle verarbeiten kann). Weitere Informationen finden Sie unter [Festlegen der Sicherheit auf Schnittstellenproxyebene.](setting-security-at-the-interface-proxy-level.md)

Bei komplexen Sicherheitsanforderungen können Sie alle Sicherheitsanforderungen programmgesteuert behandeln, anstatt COM die Verarbeitung für Sie zu erlauben. Rufen Sie dazu [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) auf, um die automatische Authentifizierung zu deaktivieren, und steuern Sie dann alle Sicherheitseinstellungen, indem Sie die Sicherheit pro Schnittstellenproxy festlegen. Weitere Informationen finden Sie unter [Setting Processwide Security with CoInitializeSecurity (Festlegen der prozessweiten Sicherheit mit CoInitializeSecurity)](setting-processwide-security-with-coinitializesecurity.md) und [Setting Security at the Interface Proxy Level (Festlegen der Sicherheit auf Schnittstellenproxyebene).](setting-security-at-the-interface-proxy-level.md)

In einigen Szenarien sollten Sie die Sicherheit vollständig deaktivieren. Sie können entscheiden, dass Ihre Anwendung keine Sicherheit benötigt, oder Sie möchten die Sicherheit während der Entwicklungszeit deaktivieren, damit Sie Sicherheitsfeatures einzeln aktivieren können. Informationen zum Deaktivieren der COM-Sicherheit finden Sie unter [Deaktivieren der Sicherheit.](turning-off-security.md)

Sicherheit in COM basiert auf Authentifizierungsdiensten, die von Sicherheitspaketen verwaltet werden. NTLMSSP funktioniert gut für viele Anwendungen, bietet aber nicht die stabilere Sicherheit, die von anderen Paketen geboten wird. Aus diesem Grund unterstützt COM das Schannel-Sicherheitspaket und das Kerberos v5-Sicherheitsprotokoll. Weitere Informationen zur Verwendung dieser Sicherheitspakete finden Sie unter [COM und Sicherheitspakete.](com-and-security-packages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




