---
title: Steuerelement Eigenschaften
description: Steuerelement Eigenschaften
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856900"
---
# <a name="control-properties"></a>Steuerelement Eigenschaften

Zusätzlich zu den Eigenschaften, die vom Steuerelement selbst definiert und implementiert werden, umfasst die ActiveX-Steuerelement Technologie auch Folgendes:

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient-Eigenschaften
</dt> <dd>

Diese werden vom Container über eine Steuerungs Client Site verfügbar gemacht, um Umgebungs Werte bereitzustellen, die für alle im Container eingebetteten Steuerelemente gelten. Beispielsweise kann ein Container eine Standard Hintergrundfarbe oder eine Standard Schriftart bereitstellen, die das Steuerelement verwenden kann. Ambient-Eigenschaften werden über **IDispatch** verfügbar gemacht, das für das Site-Objekt eines Containers implementiert ist. Der Container Ruft die [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) -Methode des Steuer Elements auf, wenn einer seiner Ambient-Eigenschaften den Wert ändert. In der Antwort muss ein Steuerelement möglicherweise seinen eigenen internen oder visuellen Zustand als Antwort aktualisieren. Der Container gibt an, welche Ambient-Eigenschaft mit dem dispid-Parameter geändert wurde, oder übergibt DISPID \_ unknown, um anzugeben, dass mehrere Umgebungs Eigenschaften geändert wurden.

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Erweiterte Eigenschaften
</dt> <dd>

Diese werden tatsächlich von einem Container implementiert, um die darin enthaltenen Steuerelemente zu umschließen und Container verwaltete Eigenschaften bereitzustellen, die so angezeigt werden, als wären Sie Native Steuerelement Eigenschaften. Der Container kann das Steuerelement aggregieren und die erweiterten Eigenschaften hinzufügen, um die Eigenschaften des Steuer Elements zu ergänzen oder zu überschreiben. Das aggregierte Objekt wird als erweitertes Steuerelement bezeichnet. Zum Container wird das erweiterte Steuerelement als Steuerelement angezeigt, und erweiterte Eigenschaften scheinen vom Steuerelement verfügbar gemacht zu werden. Der Container unterstützt ein erweitertes Steuerelement über die Client Standort Methode [**iolecontrolsite:: getextendedcontrol**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol). Die **getextendedcontrol** -Methode ermöglicht es Steuerelementen, durch die Site zum erweiterten Steuerelement Objekt zu navigieren, das für Sie durch den Container bereitgestellt wird, wenn der Container dieses Feature unterstützt. Ein Container kann neben den Seiten, die von einem Steuerelement normalerweise über [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)angegeben werden, auch Eigenschaften Seiten für seine erweiterten Steuerelemente anzeigen. Aus diesem Grund muss ein Steuerelement einen Container bitten, einen Eigenschaften Rahmen anzuzeigen, bevor das Steuerelement versucht, dies selbst zu tun. Hierfür Ruft das-Steuerelement [**iolecontrolsite:: showpropertyframe**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) auf. Wenn der Container diese Funktion implementiert, wird der Eigenschafts Rahmen selbst angezeigt. Wenn die Methode einen Fehler zurückgibt, kann das Steuerelement den Eigenschaften Rahmen anzeigen.

</dd> </dl>

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Standard Eigenschaften](standard-properties.md)
-   [Standard Schriftart Objekt](standard-font-object.md)
-   [Standard Bild Objekt](standard-picture-object.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerungsmethoden](control-methods.md)
</dt> </dl>

 

 




