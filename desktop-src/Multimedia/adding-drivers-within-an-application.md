---
title: Hinzufügen von Treibern in einer Anwendung
description: Hinzufügen von Treibern in einer Anwendung
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Audiokomprimierungs-Manager (ACM), Hinzufügen von Treibern
- ACM (Audiokomprimierungs-Manager), Hinzufügen von Treibern
- ACM-Beispiele,Hinzufügen von Treibern
- Hinzufügen von Treibern
- acmDriverAdd-Funktion
- Globale Treiber
- Lokale Treiber
- Audiokomprimierungs-Manager (ACM), globale Treiber
- ACM (Audiokomprimierungs-Manager), globale Treiber
- Audiokomprimierungs-Manager (ACM), lokale Treiber
- ACM (Audiokomprimierungs-Manager), lokale Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cce1310a487e772ac6f65680221f065335951d7d1d6c6dd22c4178c0d985f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692330"
---
# <a name="adding-drivers-within-an-application"></a>Hinzufügen von Treibern in einer Anwendung

Wenn Ihre Anwendung intern eigene Komprimierungsroutinen implementieren muss, kann die Anwendung dem ACM Treiber hinzufügen, indem sie die [**acmDriverAdd-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) aufruft. Die Anwendung implementiert den Treiber durch Bereitstellen einer Funktion, die dem [**acmDriverProc-Prototyp**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) entspricht. Nachdem die Anwendung den Treiber hinzugefügt hat, kann die Anwendung den Treiber über den ACM wie jeden anderen Treiber verwenden.

Der ACM behandelt Treiber entweder als global oder lokal. Eine Anwendung gibt an, ob ein Treiber beim Aufrufen von **acmDriverAdd** als global oder lokal hinzugefügt werden soll. Es gibt zwei Unterschiede zwischen globalen und lokalen Treibern:

-   Treiber, die als globale Treiber hinzugefügt werden, werden nicht für andere Anwendungen freigegeben.
-   Eine Anwendung kann die Priorität eines globalen Treibers (aber nicht eines lokalen Treibers) direkt ändern, indem die [**acmDriverPriority-Funktion aufruft.**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) Der ACM führt eine priorisierte Suche durch, wenn er nach einem geeigneten Treiber sucht, um eine Implementierung eines Funktionsaufrufs zur Verfügung zu stellen. Der ACM gibt lokalen Treibern immer eine höhere Priorität als globale Treiber. Der zuletzt hinzugefügte lokale Treiber hat die höchste Priorität.

 

 




