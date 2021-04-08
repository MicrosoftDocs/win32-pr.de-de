---
description: Mithilfe des Smartcard-Subsystems können Sie mit Karten kommunizieren, die ggf. nicht den ISO 7816-Spezifikationen entsprechen.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Direkt Karten Zugriffs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861984"
---
# <a name="direct-card-access-functions"></a>Direkt Karten Zugriffs Funktionen

Mithilfe des [*Smartcard*](/windows/desktop/SecGloss/s-gly) -Subsystems können Sie mit Karten kommunizieren, die ggf. nicht den ISO 7816-Spezifikationen entsprechen. Zu diesem Zweck können Sie mithilfe der folgenden Funktionen die Attribute der Kommunikation zwischen der Anwendung und der Karte steuern, indem Sie eine direkte Bearbeitung des [*Readers*](/windows/desktop/SecGloss/r-gly)auf niedriger Ebene ermöglichen.

Um diese Funktionen zu verwenden, müssen Sie einen Bezeichner für das betreffende Attribut angeben. Gültige Attribut Bezeichner und Werte finden Sie in der Tabelle 3-1 unter *Anforderungen für PC-Connected Schnittstellen Geräte*.



| Thema                                    | BESCHREIBUNG                           |
|------------------------------------------|---------------------------------------|
| [**Scardcontrol**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Bereitstellen der direkten Kontrolle des Readers. |
| [**Scardgetattrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Leser Attribute erhalten.                |
| [**Scardsegtaterb**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Festlegen des Reader-Attributs.                 |



 

 

 
