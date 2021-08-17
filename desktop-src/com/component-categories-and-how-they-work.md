---
title: Komponentenkategorien und deren Funktionsweise
description: Komponentenkategorien und deren Funktionsweise
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfd5580e12ce3d4a44ca251142e29f6eea8f9f5823cf18999f876a4ef732d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737016"
---
# <a name="component-categories-and-how-they-work"></a>Komponentenkategorien und deren Funktionsweise

Komponentenkategorien identifizieren die Funktionalitätsbereiche, die eine Softwarekomponente unterstützt und erfordert. Für jede Kategorie oder jeden identifizierten Funktionsbereich wird ein Registrierungseintrag verwendet. Jede Komponentenkategorie wird durch eine GUID (Globally Unique Identifier) identifiziert. Wenn ein Steuerelement installiert ist, registriert es sich selbst als Steuerelement in der Systemregistrierung mithilfe der Komponentenkategorie-ID für das Steuerelement. Weitere Informationen finden Sie unter [Selbstregistrierung für Steuerelemente.](self-registration-for-controls.md) Innerhalb der Steuerelemente selbstregistrierung werden auch die komponentenkategorien registriert, die implementiert werden, und die Komponentenkategorien, die ein Container unterstützen muss, um das Steuerelement erfolgreich zu hosten.

Wenn ein Steuerelementcontainer dem Benutzer Steuerelemente zum Einfügen anbietet, kann er nur die Steuerelemente auswählen und instanziieren, die in dieser Umgebung angemessen funktionieren. Wenn der Steuerelementcontainer beispielsweise keine Datenbindung unterstützt, lässt der Container nicht zu, dass der Benutzer die Steuerelemente mit einem Eintrag in der Registrierung auswählt und instanziiert, was bedeutet, dass die Kategorie der Datenbindungskomponente erforderlich ist. Ein allgemeines Dialogfeld für das Einfügen von Steuerelementen und APIs zum Verarbeiten der Registrierungseinträge ist verfügbar.

Komponentenkategorien sind nicht kumulativ oder exklusiv. Ein Steuerelement kann eine beliebige Kombination von Komponentenkategorien erfordern, um zu funktionieren. Ein Steuerelement, das keine erforderlichen Einträge für Komponentenkategorien aufweist, kann davon ausgehen, dass es in jedem Steuerelementcontainer funktionieren kann und keine bestimmte Funktionalität eines Steuerelementcontainers erfordert, damit es funktioniert.

Die folgenden Komponentenkategorien werden hier identifiziert, wo es erforderlich ist, dass detailliertere Spezifikationen der Kategorien verfügbar sind.

-   [**ISimpleFrameSite-Steuerelementeinschluss.**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)
-   Einfache Datenbindung über die [**IPropertyNotifySink-Schnittstelle.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)
-   Erweiterte Datenbindung (wie von den zusätzlichen Datenbindungsschnittstellen von VB4.0 unterstützt).
-   Visual Basic private Schnittstellen [**: IVBFormat,**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Internetfähige Steuerelemente.
-   Fensterlose Steuerelemente.

Dies ist keine endgültige Liste von Kategorien. weitere Kategorien werden wahrscheinlich in Zukunft definiert, wenn neue Anforderungen identifiziert werden. Eine aktuelle Liste der Komponentenkategorien ist bei Microsoft verfügbar. Diese Liste enthält die Komponentenkategorien, die von Microsoft identifiziert wurden, sowie alle anderen, über die Microsoft informiert wurde.

Es ist wichtig zu beachten, dass Steuerelemente versuchen sollten, in so vielen Umgebungen wie möglich zu funktionieren. Wenn möglich, sollte das Steuerelement seine Funktionalität beeinträchtigen, wenn es in einem Container platziert wird, der bestimmte Schnittstellen nicht unterstützt. Der Zweck von Komponentenkategorien besteht darin, eine Situation zu verhindern, in der das Steuerelement in einer Umgebung platziert wird, die nicht geeignet ist und das Steuerelement die gewünschte Aufgabe nicht erfüllen kann. Im Allgemeinen sollte ein Steuerelement ordnungsgemäß herabgestuft werden, wenn keine Schnittstellen vorhanden sind. Ein Steuerelement kann den Benutzer mit einem Meldungsfeld darüber informieren, dass einige Funktionen nicht verfügbar sind, oder die Funktionalität, die für einen Steuerelementcontainer erforderlich ist, eindeutig dokumentieren, um eine optimale Leistung zu erzielen.

Beachten Sie, dass ältere Steuerelemente und Container keine Komponentenkategorien verwenden und sich stattdessen darauf verlassen, dass das Schlüsselwort control für das Steuerelement in der Registrierung vorhanden ist. Um von älteren Containersteuerelementen erkannt zu werden, die möglicherweise das Schlüsselwort control in der Registrierung registrieren möchten, sollten Steuerelemententwickler überprüfen, ob das Steuerelement erfolgreich in solchen Containern gehostet werden kann, bevor sie dies tun. Container, die Komponentenkategorien verwenden, können sie erfolgreich zum Hosten älterer Steuerelemente verwenden, während die Komponentenkategorie-DLL die Zuordnung verarbeitet. Für ältere Steuerelemente catid ControlV1 ist eine separate Kategorie \_ vorhanden, sodass ein Container sie bei Bedarf optional ausschließen kann.

Da Komponentenkategorien durch GUIDs identifiziert werden, können Container, die bestimmte Funktionen bieten, über eigene Kategorie-IDs verfügen, die mithilfe eines GUID-Generierungstools generiert werden. Dies kann jedoch möglicherweise den Vorteil der Interoperabilität von Steuerelementen und Containern beeinträchtigen, sodass es bevorzugt wird, nach Möglichkeit vorhandene Komponentenkategorien zu verwenden. Anbietern wird empfohlen, sich beim Definieren neuer Komponentenkategorien zusammen zu informieren, um sicherzustellen, dass sie die allgemeinen Anforderungen des Marketplace erfüllen, und die Interoperabilität von ActiveX-Steuerelementen zu befolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 




