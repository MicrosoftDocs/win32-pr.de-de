---
title: Hinzufügen von Treibern in einer Anwendung
description: Hinzufügen von Treibern in einer Anwendung
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Audiokomprimierungs-Manager (ACM), Hinzufügen von Treibern
- ACM (Audiokomprimierungs-Manager), Hinzufügen von Treibern
- ACM-Beispiele, Hinzufügen von Treibern
- Hinzufügen von Treibern
- acmdriveradd-Funktion
- globale Treiber
- lokale Treiber
- Audiokomprimierungs-Manager (ACM), globale Treiber
- ACM (Audiokomprimierungs-Manager), globale Treiber
- Audiokomprimierungs-Manager (ACM), lokale Treiber
- ACM (Audiokomprimierungs-Manager), lokale Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036978"
---
# <a name="adding-drivers-within-an-application"></a>Hinzufügen von Treibern in einer Anwendung

Wenn Sie möchten, dass Ihre Anwendung ihre eigenen Komprimierungs Routinen intern implementiert, kann die Anwendung dem ACM Treiber hinzufügen, indem Sie die [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) -Funktion aufrufen. Die Anwendung implementiert den Treiber durch Bereitstellen einer Funktion, die dem [**acmdriverproc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) -Prototyp entspricht. Nachdem der Treiber von der Anwendung hinzugefügt wurde, kann die Anwendung den Treiber über das ACM verwenden, da er einen beliebigen anderen Treiber verwenden würde.

Der ACM behandelt Treiber entweder global oder local. Eine Anwendung gibt an, ob ein Treiber als Global oder local hinzugefügt werden soll, wenn er **acmdriveradd** aufruft. Es gibt zwei Unterschiede zwischen globalen und lokalen Treibern:

-   Treiber, die als globale Treiber hinzugefügt werden, werden nicht für andere Anwendungen freigegeben.
-   Eine Anwendung kann die Priorität eines globalen Treibers (aber nicht eines lokalen Treibers) direkt ändern, indem er die [**acmdriverpriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) -Funktion aufrufen. Der ACM führt bei der Suche nach einem geeigneten Treiber eine priorisierte Suche durch, um eine Implementierung eines Funktions Aufrufes bereitzustellen. Das ACM gibt immer höhere Priorität für lokale Treiber als globale Treiber. Der zuletzt hinzugefügte lokale Treiber hat die höchste Priorität.

 

 




