---
title: Übersicht über Steuerungs- und Steuerungscontainerrichtlinien
description: Übersicht über Steuerungs- und Steuerungscontainerrichtlinien
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2658c691e13b0a78da82fa006ed22142082e2f7eb8b04d78992943a024487a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120460"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Übersicht über Steuerungs- und Steuerungscontainerrichtlinien

Ein ActiveX-Steuerelement ist im Wesentlichen ein einfaches OLE-Objekt, das die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) unterstützt. In der Regel werden mehr Schnittstellen unterstützt, um Funktionen anzubieten, aber alle zusätzlichen Schnittstellen können als optional betrachtet werden. Daher sollte ein Steuerelementcontainer nicht darauf basieren, dass zusätzliche Schnittstellen unterstützt werden. Wenn keine zusätzlichen Schnittstellen angegeben werden, die ein Steuerelement unterstützen muss, kann ein Steuerelement effizient auf einen bestimmten Funktionsbereich abzielen, ohne dass bestimmte Schnittstellen unterstützt werden müssen, um als Steuerelement zu gelten. Wie immer bei OLE sollte unabhängig davon, ob es sich um ein Steuerelement oder einen Steuerelementcontainer handelt, nie davon ausgegangen werden, dass eine Schnittstelle verfügbar ist und die Standardkonventionen für die Rückgabeüberprüfung immer eingehalten werden sollten. Es ist wichtig, dass ein Steuerelement- oder Steuerelementcontainer ordnungsgemäß heruntergestuft wird und alternative Funktionen bietet, wenn keine erforderliche Schnittstelle verfügbar ist.

Ein ActiveX-Steuerelementcontainer muss in der Lage sein, ein minimales ActiveX Steuerelement zu hosten. sie unterstützt auch eine Reihe zusätzlicher Schnittstellen, wie in [Container](containers.md)angegeben. Es gibt eine Reihe von Schnittstellen und Methoden, die ein Container optional unterstützt, die in Funktionsbereiche gruppiert sind, die als *Komponentenkategorien* bezeichnet werden. Ein Container kann eine beliebige Kombination von Komponentenkategorien unterstützen, z. B. ist eine Komponentenkategorie für die Datenbindung vorhanden, und ein Container kann die Datenbindungsfunktionalität abhängig von den Marktanforderungen des Containers unterstützen oder nicht. Wenn ein Steuerelement Datenbindungsunterstützung von einem Container für die Funktion benötigt, wird diese Anforderung in die Registrierung eingegeben. Dadurch kann ein Steuerelementcontainer nur die Steuerelemente zum Einfügen anbieten, von denen er weiß, dass er erfolgreich hosten kann. Es ist wichtig zu beachten, dass Komponentenkategorien als Teil von OLE angegeben werden und nicht spezifisch für ActiveX Steuerelemente sind. Die Steuerelementarchitektur verwendet Komponentenkategorien, um Funktionalitätsbereiche zu identifizieren, die eine OLE-Komponente möglicherweise unterstützt. Komponentenkategorien sind nicht kumulativ oder exklusiv, sodass ein Steuerelementcontainer eine Kategorie unterstützen kann, ohne notwendigerweise eine andere zu unterstützen.

Es ist wichtig, dass Steuerelemente, die optionale Features oder spezifische Features für einen bestimmten Container erfordern, eindeutig verpackt und mit diesen Anforderungen in den Markt bringen. Ebenso müssen Container, die bestimmte Features oder Komponentenkategorien anbieten, als diese Supportebenen beim Hosten von ActiveX-Steuerelementen angeboten werden. Es wird empfohlen, dass Steuerelemente so viele Container wie möglich als Ziel verwenden und testen und ordnungsgemäß herabsetzen, um weniger oder alternative Funktionen anzubieten, wenn Schnittstellen oder Methoden nicht verfügbar sind. In einer Situation, in der ein Steuerelement seine angegebene Auftragsfunktion ohne Unterstützung einer Komponentenkategorie nicht ausführen kann, sollte diese Kategorie als Anforderung in die Registrierung eingegeben werden, um zu verhindern, dass das Steuerelement in einen ungeeigneten Container eingefügt wird.

Diese Richtlinien definieren die Schnittstellen und Methoden, die ein Steuerelement möglicherweise von einem Steuerelementcontainer unterstützt, obwohl wie immer ein Steuerelement die Rückgabewerte überprüfen sollte, wenn [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) oder andere Methoden zum Abrufen von Zeigern auf diese Schnittstellen verwendet werden. Ein Container sollte nicht erwarten, dass ein Steuerelement mehr als die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) unterstützt, und diese Richtlinien identifizieren, welche Schnittstellen ein Steuerelement unterstützen kann und was das Vorhandensein einer bestimmten Schnittstelle bedeutet.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>Warum die ActiveX-Richtlinien für Steuerelement- und Steuercontainer wichtig sind

ActiveX Steuerelemente haben sich zur primären Architektur für die Entwicklung programmierbarer Softwarekomponenten für die Verwendung in einer Vielzahl verschiedener Container entwickelt, von Softwareentwicklungstools bis hin zu Endbenutzerproduktivitätstools. Damit ein Steuerelement in einer Vielzahl von Containern gut funktioniert, muss das Steuerelement in der Lage sein, eine mindest erforderliche Funktionalität zu übernehmen, die es in allen Containern nutzen kann.

Durch Befolgen dieser Richtlinien machen Steuerungs- und Containerentwickler ihre Steuerelemente und Container zuverlässiger und interoperabler und letztendlich bessere und besser verwendbare Komponenten zum Erstellen komponentenbasierter Lösungen.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Was zu tun ist, wenn eine benötigte Schnittstelle nicht verfügbar ist

OLE-Programme sollten [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) verwenden, um Schnittstellenzeiger abzurufen, und müssen den Rückgabewert überprüfen. OLE-Anwendungen können nicht sicher davon ausgehen, dass **QueryInterface** erfolgreich ist.

Diese Anforderung gilt für alle OLE-Anwendungen. Wenn die angeforderte Schnittstelle nicht verfügbar ist (d. h. [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) gibt E \_ NOINTERFACE zurück), muss das Steuerelement oder der Container ordnungsgemäß herabgestuft werden, auch wenn dies bedeutet, dass die angegebene Auftragsfunktion nicht ausgeführt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX Steuerungs- und Steuerungscontainerrichtlinien](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




