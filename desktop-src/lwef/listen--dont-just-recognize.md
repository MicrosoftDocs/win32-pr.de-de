---
title: Lauschen, nicht einfach erkennen
description: Lauschen, nicht einfach erkennen
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b226b9172b10c70e4e699a98df49acc002dcd5add95986c9efbdf9e8f057648d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888090"
---
# <a name="listen-dont-just-recognize"></a>Lauschen, nicht einfach erkennen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Eine erfolgreiche Kommunikation umfasst mehr als die Erkennung von Wörtern. Der Dialogprozess impliziert den Austausch von Hinweise zum Signalisieren von "Turn-Taking" und "Understanding". Zeichen können Konversationsschnittstellen verbessern, indem sie Hinweise wie Kopfneigungen, Nods oder Schütteln bereitstellen, um anzugeben, wann sich die Sprach-Engine im Lauschzustand befindet und wann etwas erkannt wird. Microsoft Agent gibt beispielsweise Animationen  wieder, die dem Lauschzustand zugewiesen sind, wenn ein Benutzer die  Push-to-Talk-Abhörtaste drückt, und Animationen, die dem Hörzustand zugewiesen sind, wenn eine Äußerung erkannt wird. Stellen Sie beim Definieren Ihres eigenen Zeichens sicher, dass Sie diese Zustände erstellen und entsprechenden Animationen zuweisen. Weitere Informationen zum Entwerfen von Zeichen finden Sie unter [Entwerfen von Zeichen für Microsoft Agent.](designing-characters-for-microsoft-agent.md)

Zusätzlich zu nicht-konversiven Hinweise umfasst eine Konversation einen gemeinsamen Kontext zwischen den konversiven Parteien. Ebenso sind Spracheingabeszenarien mit Zeichen wahrscheinlicher, wenn der Kontext gut eingerichtet ist. Wenn Sie den Kontext einrichten, können Sie ähnlich klingende Ausdrücke wie "Check es in the mail" und "check my mail" besser interpretieren. Sie können es dem Benutzer auch ermöglichen, den Kontext abfragen, indem Sie einen Befehl wie "Hilfe" oder "Wo bin ich" bereitstellen, auf den Sie reagieren, indem Sie den aktuellen Kontext bzw. die letzte Aktion, die Ihre Anwendung ausgeführt hat, bzw. den aktuellen Kontext bzw. die letzte Aktion, die ihre Anwendung ausgeführt hat, bzw.

Microsoft Agent stellt Schnittstellen bereit, mit denen Sie auf die beste Übereinstimmung und die beiden nächsten besten Alternativen zugreifen können, die von der Spracherkennungs-Engine zurückgegeben werden. Darüber hinaus können Sie für alle Übereinstimmungen auf Konfidenzergebnisse zugreifen. Sie können diese Informationen verwenden, um besser zu bestimmen, was gesprochen wurde. Wenn beispielsweise die Konfidenzergebnisse der besten Übereinstimmung und der ersten Alternative nahe liegen, kann dies darauf hindeuten, dass die Sprach-Engine Schwierigkeiten hatte, den Unterschied zwischen ihnen zu erkennen. In einem solchen Fall können Sie den Benutzer bitten, die Anforderung zu wiederholen oder umzuformulieren, um die Leistung zu verbessern. Wenn jedoch die beste Übereinstimmung und die erste oder zweite Alternative den gleichen Befehl zurückgeben, wird die Anzeige der richtigen Erkennung verstärkt.

Die Art einer Konversation oder eines Dialogs impliziert, dass es eine Antwort auf gesprochene Eingaben geben sollte. Aus diesem Grund sollte auf die Eingabe eines Benutzers immer mit feedback with positivem oder visuellem Feedback reagiert werden, das darauf hinweist, dass eine Aktion ausgeführt wurde oder ein Problem aufgetreten ist, oder eine entsprechende Antwort liefert.

 

 




