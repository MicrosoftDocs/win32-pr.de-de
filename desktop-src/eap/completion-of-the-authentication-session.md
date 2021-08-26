---
title: Abschluss der Authentifizierungssitzung
description: Nach Abschluss der Authentifizierungssitzung ruft der Authentifizierungsdienst die RasEapEnd-Funktion auf, damit das Authentifizierungsprotokoll die Zuordnung seines Arbeitspuffers wieder auferkennen kann.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee29ac4c4139fc8a575e7570e3c04fbe449aa4d619cea3e096cd12dfcf19bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948470"
---
# <a name="completion-of-the-authentication-session"></a>Abschluss der Authentifizierungssitzung

Nach Abschluss der Authentifizierungssitzung ruft der Authentifizierungsdienst die [**RasEapEnd-Funktion**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) auf, damit das Authentifizierungsprotokoll die Zuordnung seines Arbeitspuffers wieder auferkennen kann. Diese Aktion wird unabhängig davon ausgeführt, ob die Authentifizierung erfolgreich war. Das Aufrufen der **RasEapEnd-Funktion** garantiert, dass keine weiteren Aufrufe des Authentifizierungsprotokolls mit diesem bestimmten Benutzer oder Kontext erfolgen, ohne zuerst [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))aufzurufen.

 

 