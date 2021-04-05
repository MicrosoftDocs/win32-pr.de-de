---
title: Legacyiaccessible-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für die Verwendung von ilegacyiaccessibleprovider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- Automatisierung der Benutzeroberfläche, Implementieren eines legacyiaccessible-Steuerelement Musters
- Benutzeroberflächenautomatisierungs, legacyibarrierefreiheits-Steuerelement Muster
- UI-Automatisierung, ilegacyiaccessibleprovider
- Ilegacyiaccessibleprovider
- Implementieren von legacyiaccessible-Steuerungs Mustern für die Benutzeroberflächen Automatisierung
- Legacyiaccessible-Steuerelement Muster
- Steuerelement Muster, ilegacyiaccessibleprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächen Automatisierung legacyiaccessible
- Steuerelement Muster, legacyiaccessible
- Schnittstellen, ilegacyiaccessibleprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712174"
---
# <a name="legacyiaccessible-control-pattern"></a>Legacyiaccessible-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für die Verwendung von [**ilegacyiaccessibleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das **legacyiaccessible** -Steuerelement Muster wird vom Microsoft-Active Accessibility für den Microsoft UI Automation-Proxy unterstützt.

Anwendungs-und Steuerungs Anbieter implementieren die [**ilegacyiaccessibleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) -Schnittstelle nie.

Das **legacyiaccessible** -Steuerungs Muster macht die [**iuiautomationlegacyiaccessiblepattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) -Schnittstelle für Benutzeroberflächenautomatisierungs-Clients verfügbar und ermöglicht den Zugriff auf die zugrunde liegende [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung für bestimmte Elemente der Benutzeroberfläche. **Iuiautomationlegacyiaccessiblepattern** unterstützt jedoch keine Methoden, die veraltet sind oder mit den Benutzeroberflächenautomatisierungs-Features redundant sind.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Member des **legacyiaccessible** -Steuerelement Musters](#members-of-the-legacyiaccessible-control-pattern)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

[**Ilegacyiaccessibleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider)wird von keiner Anwendung oder einem Steuerelement implementiert. Das Benutzeroberflächenautomatisierungs-Framework stellt automatisch die Anbieter Implementierung für einen systemeigenen Microsoft Active Accessibility Server bereit.

Das **legacyiaccessible** -Steuerungs Muster ist für Steuerelemente, die auf der Benutzeroberflächen Automatisierung basieren, nicht verfügbar.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Member des **legacyiaccessible** -Steuerelement Musters

Die folgenden Eigenschaften, Methoden und Ereignisse sind Mitglieder des **legacyiaccessible** -Steuerelement Musters. Die Hinweise gelten für Benutzeroberflächenautomatisierungs-Clients.



| Member                                                                        | Memberart | Hinweise                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildID**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Eigenschaft    | Gibt **childID \_ Self** (0) für ein nicht untergeordnetes Objekt zurück.                                                                                |
| [**DEFAULTACTION**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Eigenschaft    | Keine                                                                                                                                 |
| [**Beschreibung**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Eigenschaft    | Keine                                                                                                                                 |
| [**Hilfe**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Eigenschaft    | Keine                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Eigenschaft    | Keine                                                                                                                                 |
| [**Benennen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Eigenschaft    | Keine                                                                                                                                 |
| [**Funktion**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Eigenschaft    | Verwenden Sie die [**getroletext**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) -Funktion, um eine lokalisierte Zeichenfolge abzurufen.                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Methode      | Ruft einen [**iuiautomationelementarray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) -Schnittstellen Zeiger ab.                                |
| [**Bundesland/Kanton**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Eigenschaft    | Verwenden Sie die Funktion [**getstatetext**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) , um eine lokalisierte Zeichenfolge abzurufen.                                                  |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Eigenschaft    | Keine                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Methode      | Keine                                                                                                                                 |
| [**Getiaccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Methode      | Keine                                                                                                                                 |
| [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Methode      | Das auswahlflag ist ein Microsoft Active Accessibility **selflag** -Wert. Weitere Informationen finden Sie unter [selflag-Konstanten](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Methode      | Keine                                                                                                                                 |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




