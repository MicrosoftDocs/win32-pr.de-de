---
title: Funktionsweise von Eigenschaften
description: Funktionsweise von Eigenschaften
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Windows Media Player-Plug-ins, Echo-Beispiel Eigenschaften
- Plug-ins, Echo-Beispiel Eigenschaften
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel Eigenschaften
- DSP-Plug-ins, Echo-Beispiel Eigenschaften
- Echo DSP-Plug-in-Beispiel, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711562"
---
# <a name="how-properties-work"></a>Funktionsweise von Eigenschaften

Eigenschaftswerte werden in Element Variablen gespeichert.

Eigenschaften werden über Methoden Paare zugänglich gemacht. Eine Methode stellt die-Implementierung bereit, um den Eigenschafts Wert anzugeben. der Name beginnt mit Put \_ . Die andere Methode stellt die-Implementierung bereit, um den Eigenschafts Wert abzurufen. der Name beginnt mit get \_ . Die Schnittstellen Definition ist in Echo. idl enthalten. Die Eigenschaften Methoden Prototypen befinden sich in Echo. h. Sie werden in Echo. cpp implementiert.

In den nächsten drei Abschnitten erfahren Sie, wie Sie die vorhandenen Eigenschaften Methoden entsprechend Ihren Anforderungen ändern und wie Sie die Methoden für eine zusätzliche Eigenschaft hinzufügen.

-   [Variablen zum Speichern von Eigenschaften](variables-to-store-properties.md)
-   [Ändern der Scale-Eigenschaft](modifying-the-scale-property.md)
-   [Hinzufügen der Eigenschaft "nass Mischung"](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo-Beispiel Eigenschaften**](echo-sample-properties.md)
</dt> </dl>

 

 




