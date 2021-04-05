---
title: Anzeigen von modalen Benutzeroberflächen
description: Anzeigen von modalen Benutzeroberflächen
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player-Plug-ins, Anzeigen von Dialogfeldern und Meldungs Feldern
- Plug-ins, Anzeigen von Dialogfeldern und Meldungs Feldern
- Plug-Ins für die Benutzeroberfläche, Anzeigen von Dialogfeldern und Meldungs Feldern
- UI-Plug-ins, Anzeigen von Dialogfeldern und Meldungs Feldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714526"
---
# <a name="displaying-modal-user-interfaces"></a>Anzeigen von modalen Benutzeroberflächen

Benutzeroberflächen-Plug-ins sollten keine modalen Dialogfelder oder Meldungs Felder als Reaktion auf Methodenaufrufe von Windows Media Player anzeigen. Zeigen Sie z. b. ein Meldungs Feld nicht in der Implementierung von **iwmppluginui:: Create** an.

Wenn Sie ein Dialogfeld oder ein Meldungs Feld von einer Implementierung der UI-Plug-in-Methode anzeigen müssen, die vom Player aufgerufen wird, müssen Sie die folgenden Schritte ausführen:

1.  Registrieren Sie eine neue Fenster Meldung mithilfe von **RegisterWindowMessage**.
2.  Senden Sie die von Ihnen registrierte Fenster Meldung mithilfe von **PostMessage** an Ihr UI-Plug-in-Fenster.
3.  Zeigt das Dialogfeld oder das Meldungs Feld des Meldungs Handlers für die neue Fenster Meldung an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über das UI-Plug-in**](ui-plug-in-overview.md)
</dt> </dl>

 

 




