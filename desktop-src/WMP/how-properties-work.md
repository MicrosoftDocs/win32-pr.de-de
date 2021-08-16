---
title: Funktionsweise von Eigenschaften
description: Funktionsweise von Eigenschaften
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Windows Media Player Plug-Ins, Echo-Beispieleigenschaften
- Plug-Ins, Echo-Beispieleigenschaften
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispieleigenschaften
- DSP-Plug-Ins, Echo-Beispieleigenschaften
- Echo-DSP-Plug-In-Beispiel, Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdefea3fce39b70d20d2f100d36cc4aeb8770bd15cd5cd0bf0978cd08f2259f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339134"
---
# <a name="how-properties-work"></a>Funktionsweise von Eigenschaften

Eigenschaftswerte werden in Membervariablen gespeichert.

Eigenschaften werden durch Methodenpaare zugänglich gemacht. Eine Methode stellt die Implementierung bereit, um den Eigenschaftswert anzugeben. der Name beginnt mit put \_ . Die andere Methode stellt die Implementierung zum Abrufen des Eigenschaftswerts bereit. Der Name beginnt mit \_ get. Die Schnittstellendefinition befindet sich in Echo.idl. Die Eigenschaftenmethodenprototypen befinden sich in Echo.h. Sie werden in Echo.cpp implementiert.

In den nächsten drei Abschnitten erfahren Sie, wie Sie die vorhandenen Eigenschaftsmethoden ihren Anforderungen entsprechend ändern und die Methoden für eine zusätzliche Eigenschaft hinzufügen.

-   [Variablen zum Store Von Eigenschaften](variables-to-store-properties.md)
-   [Ändern der Scale-Eigenschaft](modifying-the-scale-property.md)
-   [Hinzufügen der Vernetzungsmischungseigenschaft](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Echo Sample Properties**](echo-sample-properties.md)
</dt> </dl>

 

 




