---
title: Häufig gestellte Fragen zu EAP
description: Hier finden Sie Antworten auf häufig gestellte Fragen (FAQs) zu den EAP-APIs, z. B. "Wie lang ist die Lebensdauer einer EAP-Authentifizierung?".
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a8b424ed195d30621c67007fc8e7d1a0882bae6ce676c70a1ca0dc93e8b846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978530"
---
# <a name="eap-frequently-asked-questions"></a>Häufig gestellte Fragen zu EAP

Das folgende Thema enthält Antworten auf häufig gestellte Fragen zu den EAP-APIs.



| Frage                                                                                        | Antwort                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wie lange ist die Lebensdauer einer EAP-Authentifizierung?                                                  | In einer typischen Situation besteht die Authentifizierung aus allem, was zwischen dem Aufruf der [**Funktionen "RaeapBegin"**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) und [**"RasEapEnd"**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) erfolgt. Wenn ein Benutzer sich für die Konfiguration eines EAP-Anbieters im RRAS-Snap-In entscheidet, besteht eine Authentifizierung aus allem, was zwischen dem Aufruf der [**Initialize-**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) und [**Uninitialize-Methoden**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) erfolgt.<br/> |
| Was ist "Gruppenrichtlinie"?                                                                         | Eine Beschreibung der Gruppenrichtlinie finden Sie unter [Gruppenrichtlinie Sammlung](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| Können EAP-Funktionen die von der Gruppenrichtlinie angegebene Konfigurationsrichtlinie überschreiben?                      | Nein, niemals. Wenn gruppenrichtlinien verwendet werden, überschreiben Gruppenrichtlinieneinstellungen immer die EAP-Konfigurationseinstellungen.                                                                                                                                                                                                                                                                                                                                                         |
| Ich muss Benutzer vor ungültigen PIN-Versuchen warnen. Ist es möglich, einen ungültigen Pincode zu erfassen? | Wenn der Benutzer die falsche PIN ein gibt, sendet Extensible Authentication Protocol-Transport Layer Security (EAP-TLS) einen Fehlercode an die VPN-Unterstützung. Sobald ein Fehlercode zurückgegeben wird, kann der Supplicant seine bevorzugte Wiederholungslogik implementieren.                                                                                                                                                                                                                    |
| Was ist EAP-Transport Level Security (EAP-TLS)?                                                 | EAP-TLS ist ein Client-Server-Protokoll, in dem unterschiedliche Zertifikatprofile in der Regel für den Client und Server verwendet werden. Weitere Informationen finden Sie unter [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Erweiterbaren Authentifizierungsprotokolls](using-extenstible-authentication-protocol.md)
</dt> </dl>