---
title: Native Active Accessibility-Implementierung
description: Benutzeroberflächenelemente, die die IAccessible-Schnittstelle implementieren, werden als native Implementierung bezeichnet.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4414fa1cd40b66b0971d7c74f484b90c62f86db64722abaabc0e8eea60b14fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859930"
---
# <a name="native-active-accessibility-implementation"></a>Native Active Accessibility-Implementierung

Benutzeroberflächenelemente, die die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren, stellen eine *native Implementierung* bereit. Obwohl die Entwicklungskosten für die Implementierung von **IAccessible** (oder einer anderen Component Object Model COM-Schnittstelle) hoch sein können, besteht der Vorteil in der vollständigen Kontrolle über die Für Clients verfügbar gemachten Informationen.

Wenn Ihre Anwendung benutzerdefinierte Steuerelemente oder andere Steuerelemente verwendet, die von Oleacc.dll nicht übermittelt werden können, müssen Sie eine native Implementierung bereitstellen.

 

 




