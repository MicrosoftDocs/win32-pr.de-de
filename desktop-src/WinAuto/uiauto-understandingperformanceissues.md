---
title: Grundlegendes zu Leistungsproblemen
description: In diesem Thema werden Leistungsprobleme im Zusammenhang mit der Verwendung der Text- und TextRange-Steuerelementmuster beschrieben.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- Clients,Grundlegendes zu Leistungsproblemen
- Clients,textbasierte Steuerelemente
- Clients,Textbereiche
- Clients,Textsteuermuster
- clients,TextRange-Steuerelementmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24846fea2f35cd9d265ab4f898b60dba2fc4e959b9a0f8bd7baea4661855f0a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861220"
---
# <a name="understanding-performance-issues"></a>Grundlegendes zu Leistungsproblemen

In diesem Thema werden Leistungsprobleme im Zusammenhang mit der Verwendung der [Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md) beschrieben.


Die [**Schnittstellen IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) und [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) basieren auf prozessübergreifenden Aufrufen. Sie bieten keinen Zwischenspeichermechanismus, um die Leistung beim Abrufen oder Verarbeiten von Textinhalten zu verbessern.

Eine Clientanwendung kann die Leistung verbessern, indem sie die [**IUIAutomationTextRange::GetText-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) verwendet, um Textblöcke mittlerer Größe abzurufen. Beispielsweise führt die Verwendung von **GetText** zum Abrufen einzelner Zeichen zu einem prozessübergreifenden Leistungstreffer für jedes Zeichen, während die Angabe einer maximalen Länge beim Aufrufen von **GetText** einen prozessübergreifenden Treffer zur Anwendung kommt, aber abhängig von der Größe des Textbereichs eine hohe Latenz haben kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung Unterstützung für Textinhalte](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Arbeiten mit textbasierten Steuerelementen](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




