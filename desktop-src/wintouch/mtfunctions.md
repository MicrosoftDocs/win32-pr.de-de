---
title: Funktionen (Windows-Eingabe Eingabe)
description: Dieser Abschnitt enthält Funktionen für die Eingabe von Windows-Eingaben.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows-Fingereingabe, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040018"
---
# <a name="functions-windows-touch-input"></a>Funktionen (Windows-Eingabe Eingabe)

Dieser Abschnitt enthält Funktionen für die Eingabe von Windows-Eingaben.

Die folgenden Funktionen werden für die Eingabe von Windows-Eingaben verwendet.



| Funktion                                                                                               | BESCHREIBUNG                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Closetouchinputhandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | Schließt ein Fingereingabe handle, gibt ihm zugeordneten Prozess Speicher frei und erklärt das Handle für ungültig.                                       |
| [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | Ruft ausführliche Informationen zu Finger Eingaben ab, die einem bestimmten Fingereingabe Handle zugeordnet sind.                                        |
| [**Istouchwindow**](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | Überprüft, ob ein angegebenes Fenster Berührungs fähig ist, und ruft optional die Modifiziererflags ab, die für die Berührungs Funktion des Fensters festgelegt wurden. |
| [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | Registriert ein Fenster als Berührungs fähig.                                                                                              |
| [**Unregistertouchwindow**](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | Registriert ein Fenster als nicht mehr als Berührungs fähig.                                                                                    |
| [SendMessage, PostMessage und verwandte Funktionen](sendmessage--postmessage--and-related-functions.md) | Enthält Überlegungen zum Weiterleiten von Nachrichten.                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eingabe Eingabe](multi-touch-input.md)
</dt> <dt>

[Leitfaden zur Eingabe der Windows-Eingabe Eingabe](guide-multi-touch-input.md)
</dt> </dl>

 

 




