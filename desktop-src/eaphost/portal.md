---
title: Extensible Authentication-Protokoll Host
description: Erfahren Sie mehr über den EAP-Host (Extensible Authentication Protocol). Weitere Informationen finden Sie unter Lauf Zeitanforderungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104102594"
---
# <a name="extensible-authentication-protocol-host"></a>Extensible Authentication-Protokoll Host

## <a name="purpose"></a>Zweck


EAPHost ist eine Microsoft Windows-Netzwerkkomponente, die eine EAP-Infrastruktur (Extensible Authentication Protocol) für die Authentifizierung von "Supplicant"-Protokollimplementierungen wie [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) und [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP) bereitstellt. Außerdem ermöglicht es die Authentifizierung mit "Authenticator"-Technologien wie Microsoft Network Policy Server (NPS). Im Gegensatz zum vorherigen IAS-Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)) unterstützt NPS den [Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP).


Mithilfe der EAPHost-APIs können sich Anwendungen mithilfe des EAPHost-Diensts authentifizieren und eine Vorlage für die Entwicklung von Konformitäten Authentifizierungsmethoden für die Verwendung mit EAPHost bereitstellen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die EAPHost-APIs werden nur in Windows Vista und höheren Betriebssystemen unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu EAPHost](about-eap-host.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[EAPHost-API-Referenz](eaphost-api-reference.md)
</dt> </dl>

 

 