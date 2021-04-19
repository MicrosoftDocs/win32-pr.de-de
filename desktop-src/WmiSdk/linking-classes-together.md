---
description: WMI-Anbieter sind in der Regel so konzipiert, dass Sie Informationen zu einem bestimmten verwalteten Objekt auf einem einzelnen Computer bereitstellen.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Verknüpfen von Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359503"
---
# <a name="linking-classes-together"></a>Verknüpfen von Klassen

WMI-Anbieter sind in der Regel so konzipiert, dass Sie Informationen zu einem bestimmten verwalteten Objekt auf einem einzelnen Computer bereitstellen. Wenn eine gemeinsame Eigenschaft vorhanden ist, die als Schlüssel zur eindeutigen Identifizierung aller verschiedenen Quell Instanzen dienen kann, verwenden Sie den [Ansichts Anbieter](view-provider.md) , um Eigenschaften aus unterschiedlichen Klassen, Namespaces oder Computern zu einer einzigen Klasse zu kombinieren.

Sie müssen [den Ansichts Anbieter zunächst registrieren](registering-the-view-provider.md). Nach der Registrierung können Sie die folgenden Typen von Ansichts Klassen erstellen:

-   [Joinansicht](creating-a-new-instance-from-old-properties.md)

    Instanzen von verschiedenen Klassen, die durch einen allgemeinen Eigenschafts Wert verbunden sind.

-   [Zuordnungs Ansicht](associating-instances-between-namespaces.md)

    Sichten vorhandener Zuordnungs Klassen über der Namespace Grenze hinweg.

-   [Union-Ansicht](creating-a-union-view-class.md)

    Union von einer oder mehreren-Instanzen.

 

 



