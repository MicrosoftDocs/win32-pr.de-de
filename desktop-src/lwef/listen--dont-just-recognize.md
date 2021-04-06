---
title: Lauschen, nicht nur erkennen
description: Lauschen, nicht nur erkennen
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e972a8c98460e58d0f7080d7de7641fb856c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713872"
---
# <a name="listen-dont-just-recognize"></a>Lauschen, nicht nur erkennen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die erfolgreiche Kommunikation umfasst mehr als das Erkennen von Wörtern. Der Prozess des Dialogs impliziert das Austauschen von Cues, um das umwandeln und verstehen zu signalisieren. Zeichen können die konvertisierungsschnittstellen verbessern, indem Sie Hinweise wie Head-Tilts, Nods oder Shakes bereitstellen, um anzugeben, wann sich die Sprach-Engine im Empfangs Zustand befindet und wann etwas erkannt wird. Der Microsoft-Agent gibt beispielsweise Animationen wieder, die dem **Überwachungszustand zugewiesen** sind, wenn ein Benutzer den Push-to-Talk-Abhör Schlüssel und die Animationen drückt, die dem **hörzustand** zugewiesen sind, wenn eine Äußerung erkannt wird. Wenn Sie ein eigenes Zeichen definieren, stellen Sie sicher, dass Sie entsprechende Animationen erstellen und diesen Zuständen zuweisen. Weitere Informationen zum Entwerfen von Zeichen finden Sie unter [Entwerfen von Zeichen für den Microsoft-Agent](designing-characters-for-microsoft-agent.md).

Zusätzlich zu nicht verbalen hinweisen umfasst eine Konversation einen gemeinsamen Kontext zwischen den Konversation-Parteien. Ebenso sind Spracheingabe Szenarios mit Zeichen wahrscheinlicher, wenn der Kontext gut eingerichtet ist. Das Einrichten des Kontexts ermöglicht es Ihnen, ähnlich klingende Ausdrücke wie "Einchecken in der e-Mail" und "meine e-Mail überprüfen" besser zu interpretieren. Sie können es dem Benutzer auch ermöglichen, den Kontext abzufragen, indem Sie einen Befehl wie "Help" oder "Where am I" bereitstellen, auf den Sie Antworten, indem Sie den aktuellen Kontext erneut angeben, z. b. die letzte Aktion, die von der Anwendung ausgeführt wurde.

Der Microsoft-Agent stellt Schnittstellen bereit, mit denen Sie auf die beste Entsprechung und die beiden nächsten Alternativen Alternativen zugreifen können. Außerdem können Sie auf Vertrauens Ergebnisse für alle Übereinstimmungen zugreifen. Anhand dieser Informationen können Sie besser bestimmen, was gesprochen wurde. Wenn z. b. die Vertrauenswürdigkeit der besten und ersten alternativen nah beieinander liegen, kann dies darauf hindeuten, dass die Sprach-Engine den Unterschied zwischen Ihnen nicht erkennen konnte. In einem solchen Fall können Sie den Benutzer bitten, die Anforderung zu wiederholen oder neu zu formulieren, um die Leistung zu verbessern. Wenn jedoch die beste Übereinstimmung und die erste oder zweite Alternative den gleichen Befehl zurückgeben, wird die Angabe der richtigen Erkennung verstärkt.

Die Art einer Konversation oder eines Dialogs impliziert, dass eine Antwort auf die gesprochene Eingabe vorhanden sein sollte. Aus diesem Grund sollte die Eingabe eines Benutzers stets mit einem verbalen oder visuellen Feedback beantwortet werden, das angibt, dass eine Aktion ausgeführt wurde oder ein Problem aufgetreten ist, oder eine entsprechende Antwort bereitstellt.

 

 




