---
title: Häufig gestellte Fragen zu EAP
description: Hier finden Sie Antworten auf häufig gestellte Fragen (FAQs) zu den EAP-APIs, wie z. b. "wie lautet die Lebensdauer einer EAP-Authentifizierung?".
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08713b17491d4b0bd76540c09b9d4588116256f
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "103949274"
---
# <a name="eap-frequently-asked-questions"></a>Häufig gestellte Fragen zu EAP

Im folgenden Thema finden Sie Antworten auf häufig gestellte Fragen zu den EAP-APIs.



| Frage                                                                                        | Antwort                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Was ist die Lebensdauer einer EAP-Authentifizierung?                                                  | In einer typischen Situation besteht die Authentifizierung aus allen Funktionen, die zwischen dem Aufrufen der Funktionen [**rapeer apbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) und [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) auftreten. Wenn ein Benutzer sich dafür entscheidet, einen EAP-Anbieter im RRAS-Snap-in zu konfigurieren, besteht eine Authentifizierung aus allen Informationen, die zwischen dem Aufrufen der Methoden [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) und [**Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) auftreten.<br/> |
| Was ist "Gruppenrichtlinie"?                                                                         | Eine Beschreibung der Gruppenrichtlinie finden Sie unter [Gruppenrichtlinie Sammlung](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| Können EAP-Funktionen die von der Gruppenrichtlinie angegebene Konfigurationsrichtlinie außer Kraft setzen?                      | Nein, niemals. Wenn die Gruppenrichtlinie verwendet wird, werden die EAP-Konfigurationseinstellungen von Gruppenrichtlinien Einstellungen immer überschrieben.                                                                                                                                                                                                                                                                                                                                                         |
| Ich muss die Benutzer über ungültige Pin-Versuche warnen. Ist es möglich, einen ungültigen PIN-Code zu erfassen? | Wenn der Benutzer die falsche PIN eingibt, sendet die erweiterbare Authentifizierung Protocol-Transport Layer Security (EAP-TLS) einen Fehlercode an den VPN-Supplicant. Sobald ein Fehlercode zurückgegeben wird, kann der Supplicant seine bevorzugte Wiederholungs Logik implementieren.                                                                                                                                                                                                                    |
| Was ist EAP-Transport Level Security (EAP-TLS)?                                                 | EAP-TLS ist ein Client/Server-Protokoll, bei dem unterschiedliche Zertifikat Profile in der Regel für den Client und den Server verwendet werden. Weitere Informationen finden Sie unter [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Extensible Authentication-Protokolls](using-extenstible-authentication-protocol.md)
</dt> </dl>