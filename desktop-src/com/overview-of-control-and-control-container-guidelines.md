---
title: Übersicht über Steuerelement-und Steuerungs Container-Richtlinien
description: Übersicht über Steuerelement-und Steuerungs Container-Richtlinien
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd72851775898f4fd140c7d101d72993c34e3eb
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103720048"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Übersicht über Steuerelement-und Steuerungs Container-Richtlinien

Ein ActiveX-Steuerelement ist im Grunde ein einfaches OLE-Objekt, das die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützt In der Regel werden weitere Schnittstellen unterstützt, um Funktionen bereitzustellen. Allerdings können alle weiteren Schnittstellen als optional angezeigt werden. Daher sollte ein Steuerelement Container nicht auf Weitere unterstützte Schnittstellen zurückgreifen. Wenn keine zusätzlichen Schnittstellen angegeben werden, die von einem Steuerelement unterstützt werden müssen, kann ein Steuerelement einen bestimmten Funktionsbereich effizient ausrichten, ohne bestimmte Schnittstellen zur Qualifizierung als Steuerelement zu unterstützen. Wie immer bei OLE, egal ob in einem Steuerelement oder einem Steuerelement Container, sollte niemals davon ausgegangen werden, dass eine Schnittstelle verfügbar ist und dass Standard Konventionen für die Rückgabe Überprüfung immer befolgt werden sollten. Es ist wichtig, dass ein Steuerelement-oder Steuerelement Container ordnungsgemäß herabgestuft wird und alternative Funktionen bietet, wenn eine erforderliche Schnittstelle nicht verfügbar ist.

Ein ActiveX-Steuerelement Container muss ein minimales ActiveX-Steuerelement hosten können. Er unterstützt auch eine Reihe zusätzlicher Schnittstellen, wie in [Containern](containers.md)angegeben. Es gibt eine Reihe von Schnittstellen und Methoden, die möglicherweise von einem Container unterstützt werden, die in funktionale Bereiche gruppiert werden, die als *Komponenten Kategorien* bezeichnet werden. Ein Container kann eine beliebige Kombination von Komponenten Kategorien unterstützen, z. b. eine Komponenten Kategorie für die Datenbindung, und ein Container unterstützt die Daten Bindungs Funktionalität abhängig von den Marktanforderungen des Containers. Wenn ein Steuerelement eine Datenbindung von einem Container zur Funktionsweise benötigt, wird diese Anforderung in die Registrierung eingegeben. Dies ermöglicht es einem Steuerelement Container, nur solche Steuerelemente einzufügen, die er erfolgreich hosten kann. Es ist wichtig zu beachten, dass Komponenten Kategorien als Teil von OLE angegeben werden und nicht spezifisch für ActiveX-Steuerelemente sind. in der Architektur der Steuerelemente werden Komponenten Kategorien verwendet, um Funktionsbereiche zu identifizieren, die von einer OLE-Komponente unterstützt werden. Komponenten Kategorien sind nicht kumulativ oder exklusiv, sodass ein Steuerungs Container eine Kategorie unterstützen kann, ohne dass ein anderer unterstützt wird.

Es ist wichtig für Steuerelemente, die optionale Features erfordern, oder für einen bestimmten Container spezifische Features, die mit diesen Anforderungen eindeutig verpackt und vermarktet werden müssen. Auf ähnliche Weise müssen Container, die bestimmte Features oder Komponenten Kategorien anbieten, beim Hosten von ActiveX-Steuerelementen als Unterstützung für diese Unterstützung angeboten werden. Es wird empfohlen, dass Sie das Ziel und den Test mit so vielen Containern wie möglich Steuern und die Abstufung von weniger oder alternativen Funktionen durchzuführen, wenn keine Schnittstellen oder Methoden verfügbar sind. In einer Situation, in der ein Steuerelement die festgelegte Auftrags Funktion ohne die Unterstützung einer Komponenten Kategorie nicht ausführen kann, sollte diese Kategorie als Anforderung in die Registrierung eingegeben werden, um zu verhindern, dass das Steuerelement in einen nicht geeigneten Container eingefügt wird.

Diese Richtlinien definieren die Schnittstellen und Methoden, die ein Steuerelement in einem Steuerelement Container möglicherweise erwartet, obwohl ein Steuerelement immer die Rückgabewerte überprüfen sollte, wenn [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) oder andere Methoden zum Abrufen von Zeigern auf diese Schnittstellen verwendet werden. Ein Container sollte nicht erwarten, dass ein Steuerelement mehr als die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle unterstützt, und diese Richtlinien bestimmen, welche Schnittstellen ein Steuerelement unterstützen kann und was das vorhanden sein einer bestimmten Schnittstelle bedeutet.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>Warum die Richtlinien für ActiveX-Steuerelement und Steuerelement Container wichtig sind

ActiveX-Steuerelemente sind die primäre Architektur zum entwickeln programmierbarer Softwarekomponenten für die Verwendung in einer Vielzahl verschiedener Container, von Software Entwicklungs Tools bis hin zu Endbenutzer-Produktivitäts Tools. Damit ein Steuerelement gut in einer Vielzahl von Containern eingesetzt werden kann, muss das Steuerelement in der Lage sein, ein gewisses Maß an Funktionalität anzunehmen, auf das es in allen Containern basieren kann.

Wenn Sie diese Richtlinien befolgen, stellen Steuerelemente und Container Entwickler ihre Steuerelemente und Container zuverlässiger und interoperable und letztendlich bessere und nutzlichere Komponenten zum Erstellen von komponentenbasierten Lösungen dar.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>Was Sie tun müssen, wenn eine benötigte Schnittstelle nicht verfügbar ist

OLE-Programme sollten [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) zum Abrufen von Schnittstellen Zeigern verwenden und den Rückgabewert überprüfen. OLE-Anwendungen können nicht sicher davon ausgehen, dass **QueryInterface** erfolgreich ist.

Diese Anforderung gilt für alle OLE-Anwendungen. Wenn die angeforderte Schnittstelle nicht verfügbar ist (d. h., [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) gibt E \_ nointerface zurück), muss das Steuerelement oder der Container ordnungsgemäß herabgestuft werden, auch wenn dies bedeutet, dass die vorgesehene Auftrags Funktion nicht durchgeführt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelement-und Steuerelement Container](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




