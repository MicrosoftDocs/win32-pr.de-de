---
title: Mehrere Steuerelemente in einer DLL
description: Mehrere Steuerelemente in einer DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b571f307f3438ca8f8ce0a0a716af2042884520cd07746f8e6fa8c1739fae22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130062"
---
# <a name="multiple-controls-in-one-dll"></a>Mehrere Steuerelemente in einer DLL

Eine einzelne OCX-DLL kann eine beliebige Anzahl von ActiveX-Steuerelementen containern, wodurch die Verteilung und Verwendung einer Reihe verwandter Steuerelemente vereinfacht wird.

Wenn Sie mehrere Steuerelemente in einer einzelnen DLL versenden, stellen Sie sicher, dass Sie den Herstellernamen in jeden Steuerelementnamen in das Paket einbetten. Durch die Einbeziehung der Herstellernamen in jeden Steuerelementnamen können Benutzer Steuerelemente innerhalb eines Pakets leicht identifizieren. Wenn Sie beispielsweise eine DLL mit drei Steuerelementen (Con1, Con2 und Con3) versenden, sollten die Steuerelementnamen wie die folgenden sein:

-   *Name Ihres Unternehmens* Con1-Steuerelement

-   *Name Ihres Unternehmens* Con2-Steuerelement

-   *Name Ihres Unternehmens* Con3-Steuerelement

 

 




