---
title: ObjectModel-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von iobjectmodelprovider, einschließlich Informationen zu-Methoden. Das ObjectModel-Steuerelement Muster wird verwendet, um einen Zeiger auf das zugrunde liegende Objektmodell eines Dokuments verfügbar zu machen.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des ObjectModel-Steuerelement Musters
- UI-Automatisierung, ObjectModel-Steuerelement Muster
- UI-Automatisierung, iobjectmodelprovider
- IObjectModelProvider
- Implementieren eines ObjectModel-Steuerelement Musters
- ObjectModel-Steuerelement Muster
- Steuerelement Muster, iobjectmodelprovider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-ObjectModel
- Steuerelement Muster, ObjectModel
- Schnittstellen, iobjectmodelprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315782"
---
# <a name="objectmodel-control-pattern"></a>ObjectModel-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**iobjectmodelprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), einschließlich Informationen zu-Methoden. Das **ObjectModel** -Steuerelement Muster wird verwendet, um einen Zeiger auf das zugrunde liegende Objektmodell eines Dokuments verfügbar zu machen.

Viele Anwendungen implementieren umfassende Objekt Modelle, die über die von der Microsoft-Benutzeroberflächen Automatisierung bereitgestellte Werte hinaus erhöhen. Dieses Steuerelement Muster ermöglicht einem Client, von einem Benutzeroberflächenautomatisierungs-Element in das zugrunde liegende-Objektmodell zu navigieren.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **iobjectmodelprovider**](#required-members-for-iobjectmodelprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ObjectModel** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Die [**iobjectmodelprovider:: getunderlyingobjectmodel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) -Methode sollte einen Zeiger auf das Objekt zurückgeben, das so nah wie möglich an das Quell-UI-Element ist. Beispielsweise sollte ein Benutzeroberflächenautomatisierungs-Anbieter für ein einzelnes Element in einem Webbrowser einen Objektmodell Zeiger für das Element zurückgeben. Das Zurückgeben eines Objektmodell Zeigers für den Dokument Stamm wäre weitaus weniger nützlich.
-   Es wird erwartet, dass der Client des **ObjectModel** -Steuerelement Musters über die IID für die Schnittstelle verfügt, die Sie suchen. aus diesem Grund genügt es, einen einfachen [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Zeiger zurückzugeben.
-   Da die Benutzeroberflächen Automatisierung den Zeiger auf den Client Prozess Marshalls, sollte der Anbieter den Zugriff auf das Objektmodell unter Verwendung von Standard-Component Object Model-Methoden (com) erwarten.

## <a name="required-members-for-iobjectmodelprovider"></a>Erforderliche Member für **iobjectmodelprovider**

Zum Implementieren der [**iobjectmodelprovider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) -Schnittstelle ist die folgende Methode erforderlich.



| Erforderliche Member                                                                             | Memberart | Hinweise                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getunderlyingobjectmodel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Methode      | Gibt einen com-Zeiger auf das zugrunde liegende Objektmodell zurück. Der Client wird erwartet, dass die [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode aufgerufen wird, um bestimmte Objektmodell Zeiger abzurufen. |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 