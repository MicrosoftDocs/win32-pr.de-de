---
title: Grundlegendes zu Leistungsproblemen
description: In diesem Thema werden Leistungsprobleme im Zusammenhang mit Text-und TextRange-Steuerelement Mustern beschrieben.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- Clients, Grundlegendes zu Leistungsproblemen
- Clients, textbasierte Steuerelemente
- Clients, Textbereiche
- Clients, Text-Steuerelement Muster
- Clients, TextRange-Steuerelement Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316826"
---
# <a name="understanding-performance-issues"></a>Grundlegendes zu Leistungsproblemen

In diesem Thema werden Leistungsprobleme im Zusammenhang mit [Text-und TextRange-](uiauto-implementingtextandtextrange.md) Steuerelement Mustern beschrieben.


Die [**iuiautomationtextpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) -Schnittstelle und die [**iuiautomationtextrange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) -Schnittstelle basieren auf prozessübergreifenden aufrufen – Sie bieten keinen Cachingmechanismus, um die Leistung beim Abrufen oder Verarbeiten von Textinhalten zu verbessern.

Eine Client Anwendung kann die Leistung verbessern, indem die [**iuiautomationtextrange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) -Methode verwendet wird, um Textblöcke mit mittlerer Größe abzurufen. Wenn Sie z. b. **gettext** zum Abrufen von einzelnen Zeichen verwenden, wird für jedes Zeichen eine prozessübergreifende Leistungs Einbuße ausgelöst, während beim Aufrufen von **gettext** keine maximale Länge angegeben wird. Dies kann je nach Größe des Text Bereichs eine hohe Latenz verursachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text-und TextRange-Steuerelement Muster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit Text basierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




