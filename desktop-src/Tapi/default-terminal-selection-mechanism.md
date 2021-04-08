---
description: Das Konzept des Multitrack-Terminals macht es für TAPI noch besser erwünscht, eine vereinfachte Methode zum Auswählen eines Terminals für einen Stream oder Datenströme bereitzustellen. Der standardmäßige Terminal Auswahlmechanismus ist darauf ausgerichtet, dies zu beheben.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Standardmäßiger Terminal Auswahlmechanismus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862255"
---
# <a name="default-terminal-selection-mechanism"></a>Standardmäßiger Terminal Auswahlmechanismus

Das Konzept des [Multitrack-Terminals](multitrack-terminals.md) macht es für TAPI noch besser erwünscht, eine vereinfachte Methode zum Auswählen eines Terminals für einen Stream oder Datenströme bereitzustellen. Der standardmäßige Terminal Auswahlmechanismus ist darauf ausgerichtet, dies zu beheben.

## <a name="selecting-a-terminal-on-a-call"></a>Auswählen eines Terminals bei einem Telefon

Das standardmäßige Terminal Auswahl Feature wird über die Möglichkeit zur Auswahl eines Terminals bei einem-Befehl bereitgestellt.

Das [callsobjekt](call-object.md) macht eine neue Schnittstelle verfügbar, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). Die-Schnittstelle macht dieselben Methoden wie [**itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)sowie drei neue Methoden verfügbar: [**requestterminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**selectterminaloncallund**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) [**unselectterminaloncall.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall)

**ITBasicCallControl2:: requestterminal** erstellt ein Terminal mit der angegebenen Terminal Klasse, Richtung und dem Medientyp. Die Liste der unterstützten statischen und dynamischen Terminals wird durchsucht, um das angeforderte Terminal zu finden und zu erstellen.

[**ITBasicCallControl2:: selectterminaloncallwählt**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) das Terminal aus (oder im Fall eines Multitrack-Terminals zählt, erstellt, erstellt und wählt die nach Verfolgungs Terminals) für den Stream (oder die Streams), der für den-Befehl verfügbar ist.

Der Algorithmus für das Abgleichen von callstreams zum Terminal (oder im Terminal verfügbarer Titel) wird in der Dokumentation für [**ITBasicCallControl2:: selectterminaloncallbeschrieben**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

Das Aufrufen von [**ITBasicCallControl2:: unselectterminaloncall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) bewirkt, dass das Terminal (Single-Track oder Multitrack) im Aufruf deaktiviert wird. Weitere Informationen finden Sie in der Dokumentation der-Methode.

## <a name="selecting-a-terminal-on-itstream"></a>Auswählen eines Terminals für itstream

Wenn Sie ein Single-Track-Terminal auf [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) auswählen (durch Aufrufen von [**itstream:: selectterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)), wird das Terminal im Stream ausgewählt. Dies ist die übliche TAPI 3-Terminal Auswahl Prozedur.

In einem Datenstrom können nur Einzeltitel Terminals ausgewählt werden. Das Auswählen eines Multitrack-Terminals für einen Stream schlägt fehl, da der Stream den Medientyp und die Richtung nicht erkennt.

 

 
