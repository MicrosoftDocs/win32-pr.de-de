---
description: WMI-Anbieter sind in der Regel darauf ausgelegt, Informationen zu einem bestimmten verwalteten Objekt auf einem einzelnen Computer bereitzustellen.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Verknüpfen von Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da48ab6b816eece1184915026ca32ed152b896f0555ca6c546d0b8ed4d6a7640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131222"
---
# <a name="linking-classes-together"></a>Verknüpfen von Klassen

WMI-Anbieter sind in der Regel darauf ausgelegt, Informationen zu einem bestimmten verwalteten Objekt auf einem einzelnen Computer bereitzustellen. Wenn es eine gemeinsame Eigenschaft gibt, die als Schlüssel zum eindeutigen Identifizieren aller verschiedenen Quellinstanzen dienen kann, verwenden Sie den [Ansichtsanbieter,](view-provider.md) um Eigenschaften aus verschiedenen Klassen, Namespaces oder Computern in einer einzelnen Klasse zu kombinieren.

Sie müssen zuerst [den Ansichtsanbieter registrieren.](registering-the-view-provider.md) Nach der Registrierung können Sie die folgenden Typen von Ansichtsklassen erstellen:

-   [Join-Ansicht](creating-a-new-instance-from-old-properties.md)

    Instanzen verschiedener Klassen, die durch einen gemeinsamen Eigenschaftswert verbunden sind.

-   [Zuordnungsansicht](associating-instances-between-namespaces.md)

    Ansichten vorhandener Zuordnungsklassen über die Namespacegrenze hinweg.

-   [Union-Ansicht](creating-a-union-view-class.md)

    Vereinigung einer oder mehrerer Instanzen.

 

 



