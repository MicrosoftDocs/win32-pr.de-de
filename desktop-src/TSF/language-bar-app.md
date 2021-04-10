---
title: Sprach Leiste (TSF-Anwendungen)
description: Eine Anwendung kann der sprach Leiste keine Elemente hinzufügen. nur ein Text Dienst kann der sprach Leiste Elemente hinzufügen.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Text Services-Framework (TSF), sprach Leiste
- TSF (Text Dienst Framework), sprach Leiste
- TSF-aktivierte Anwendungen, sprach Leiste
- sprach Leiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858618"
---
# <a name="language-bar-tsf-applications"></a>Sprach Leiste (TSF-Anwendungen)

Eine Anwendung kann der sprach Leiste keine Elemente hinzufügen. nur ein Text Dienst kann der sprach Leiste Elemente hinzufügen. Eine Anwendung kann Einfluss darauf haben, wie bestimmte Elemente in der sprach Leiste angezeigt werden.

Mit dem " [GUID Depot \_ \_ Speech \_ ](predefined-compartments.md) "-Depot wird der Typ der Spracheingabe angegeben, die von der Anwendung akzeptiert werden kann: direkt Texteingabe (Diktat) und/oder Sprachbefehle. Standardmäßig ist das Diktat aktiviert, und der Sprachbefehl ist deaktiviert. Wenn die Anwendung Sprachbefehle akzeptieren kann, sollte Sie den Wert für den TF-Befehl [ \_ \_ aktivieren](speech-recognition-constants.md) , der in der Sprachausgabe des GUID-Depots abgelegt wurde \_ \_ \_ . Wenn die Anwendung eine Diktat Annahme akzeptieren kann, sollte Sie den Wert für die TF- \_ Diktat \_ Aktivierung in der Sprachausgabe des GUID-Depots festlegen \_ \_ \_ . Der TF- \_ Diktat \_ für den Wert oder der TF- \_ \_ Befehl für den Wert dieses Depots bestimmt, welche Mode-(Diktat-oder Befehls) Spracheingaben derzeit in ausgeführt werden.

Wenn die Anwendung persistente Speicherung von Eigenschafts Daten unterstützt, sollte das [GUID-Depot \_ \_ persistmenuaktiviertes](predefined-compartments.md) Depot auf einen Wert ungleich 0 (null) festgelegt werden. Dies bewirkt, dass der sprach Text Dienst das Menü Element " **Sprach Daten speichern** " aktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten des Text Dienst-Frameworks](how-to-set-up-tsf.md)
</dt> <dt>

[Sprach Leiste (Text Dienste)](language-bar.md)
</dt> </dl>

 

 




