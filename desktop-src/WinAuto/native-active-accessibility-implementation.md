---
title: Native Active Accessibility-Implementierung
description: Benutzeroberflächen Elemente, die die IAccessible-Schnittstelle implementieren, stellen eine native Implementierung dar.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339415"
---
# <a name="native-active-accessibility-implementation"></a>Native Active Accessibility-Implementierung

Benutzeroberflächen Elemente, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren, stellen eine *native Implementierung* dar. Obwohl die Entwicklungskosten für die Implementierung von **IAccessible** (oder einer beliebigen anderen Component Object Model (com)-Schnittstelle) hoch sein können, ist der Vorteil die umfassende Kontrolle über die Informationen, die Clients zur Verfügung gestellt werden.

Wenn Ihre Anwendung benutzerdefinierte Steuerelemente oder andere Steuerelemente verwendet, die nicht von Oleacc.dll bereitgestellt werden können, müssen Sie eine systemeigene Implementierung bereitstellen.

 

 




