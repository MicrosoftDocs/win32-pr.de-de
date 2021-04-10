---
title: Webanwendungsproxy
description: Webanwendungsproxy
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104102466"
---
# <a name="web-application-proxy"></a>Webanwendungsproxy

## <a name="platform"></a>Plattform

**Server:** Windows Server 2012 R2  






## <a name="description"></a>BESCHREIBUNG

In Windows Server 2012 R2 haben wir einen neuen Dienst mit dem Namen "webanwendungsproxy" unter der Remote Zugriffs Rolle hinzugefügt, mit dem Administratoren Anwendungen für den externen Zugriff veröffentlichen können. Dieser Dienst fungiert als Reverseproxy und als Active Directory-Verbunddienste (AD FS)-Proxy (AD FS). Tatsächlich ersetzt dieser Dienst den AD FS Proxy Dienst, wie er in Windows Server 2012 bekannt war.

Mit dem webanwendungsproxy kann eine Organisation lokale Webressourcen für den externen Zugriff verfügbar machen, während gleichzeitig das Risiko dieses Zugriffs durch Steuern der Authentifizierungs-und Autorisierungs Richtlinien auf dem AD FS verwaltet wird.

## <a name="manifestation"></a>Ausstrahlung

Der AD FS Proxy Dienst befindet sich nicht mehr in der Active Directory-Verbunddienste (AD FS)-Rolle (AD FS), sondern wurde durch den webanwendungsproxy unter der Remote Zugriffs Rolle ersetzt. Dies stellt eine Erweiterung des AD FS Proxy Dienstanbieter durch Einschließen von Reverseproxyfunktionen für die Anwendungs Veröffentlichung dar.

## <a name="solution"></a>Lösung

Für den Zugriff auf den webanwendungsproxy können Administratoren zu Server-Manager wechseln und eine neue Rolle/einen neuen Rollen Dienst hinzufügen. Der Administrator findet den webanwendungsproxy unter der Remote Zugriffs Rolle.

## <a name="resources"></a>Ressourcen

-   [Lösungsanleitung](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 