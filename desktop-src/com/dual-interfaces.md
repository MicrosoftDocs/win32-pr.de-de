---
title: Duale Schnittstellen (com)
description: Duale Schnittstellen
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039718"
---
# <a name="dual-interfaces"></a>Duale Schnittstellen

OLE-Automatisierung ermöglicht einem Objekt, eine Reihe von Methoden auf zwei Arten verfügbar zu machen: über die **IDispatch** -Schnittstelle und durch direkte OLE-Vtable-Bindungen. **IDispatch** wird von den meisten Tools verwendet, die heute verfügbar sind, und bietet Unterstützung für das späte Binden an Eigenschaften und Methoden.

Die Vtable-Bindung bietet eine wesentlich höhere Leistung, da diese Methode direkt anstelle von **IDispatch:: Aufrufen** aufgerufen wird. **IDispatch** bietet eine spät gebundene Unterstützung, bei der die direkte Vtable-Bindung einen erheblichen Leistungsgewinn bietet. Beide Techniken sind wertvoll und in verschiedenen Szenarien wichtig. Durch das bezeichnen einer Schnittstelle als \[ [**Dual**](/windows/desktop/Midl/dual) \] in der Typbibliothek kann eine OLE-Automatisierungsschnittstelle entweder über **IDispatch** oder direkt an gebunden werden. Container können daher die am besten geeignete Methode auswählen. Die Unterstützung für duale Schnittstellen wird für Steuerelemente und Container dringend empfohlen.

 

 