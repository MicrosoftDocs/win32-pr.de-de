---
title: Mehrere Steuerelemente in einer dll
description: Mehrere Steuerelemente in einer dll
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036394"
---
# <a name="multiple-controls-in-one-dll"></a>Mehrere Steuerelemente in einer dll

Eine einzelne. ocx-dll kann eine beliebige Anzahl von ActiveX-Steuerelementen Container und somit die Verteilung und Verwendung eines Satzes verwandter Steuerelemente vereinfachen.

Wenn Sie mehrere Steuerelemente in einer einzelnen dll versenden, achten Sie darauf, dass Sie den Herstellernamen in jedem Steuerelement Namen in das Paket einschließen. Wenn Sie die Namen der Lieferanten in die einzelnen Steuerelement Namen einschließen, können Benutzer Steuerelemente in einem Paket problemlos identifizieren. Wenn Sie z. b. eine DLL bereitstellen, die drei Steuerelemente, Con1, Con2 und Con3 implementiert, sollten die Namen der Steuerelemente wie folgt lauten:

-   *Name Ihres Unternehmens* Con1-Steuerelement

-   *Name Ihres Unternehmens* Con2-Steuerelement

-   *Name Ihres Unternehmens* Con3-Steuerelement

 

 




