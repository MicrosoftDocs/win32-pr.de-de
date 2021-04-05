---
title: Objekt Navigations Eigenschaften und-Methoden
description: Clients Navigieren von einem Objekt zu einem anderen mithilfe von Methoden wie IAccessible accNavigate und IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947613"
---
# <a name="object-navigation-properties-and-methods"></a>Objekt Navigations Eigenschaften und-Methoden

Clients *Navigieren* von einem Objekt zu einem anderen mithilfe von Methoden wie [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) und [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Diese Methoden ermöglichen es Clients, entweder eine untergeordnete ID oder die Adresse der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle eines anderen Objekts abzurufen. Mithilfe der Navigation können Clients untersuchen, wie Objekte miteinander in Beziehung stehen. Beachten Sie, dass beim Navigieren zu einem anderen Objekt die Auswahl oder der Fokus nicht geändert wird.

Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle stellt Eigenschaften und Methoden bereit, die die folgenden Arten der Navigation unterstützen:

-   [Hierarchische Navigation](hierarchical-navigation.md)
-   [Räumliche und logische Navigation](spatial-and-logical-navigation.md)
-   [Navigation durch Treffer Tests und Bildschirmposition](navigation-through-hit-testing-and-screen-location.md)

 

 




