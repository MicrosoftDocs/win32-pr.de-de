---
title: Serialisierungsstile
description: Es gibt drei Stile, die Sie verwenden können, um serialisierungshandles zu bearbeiten.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388516"
---
# <a name="serialization-styles"></a>Serialisierungsstile

Es gibt drei Stile, die Sie verwenden können, um serialisierungshandles zu bearbeiten. Diese lauten wie folgt:

-   [Serialisierung fester Puffer](fixed-buffer-serialization.md)
-   [Dynamische pufferserialisierung](dynamic-buffer-serialization.md)
-   [Krementelle Serialisierung](incremental-serialization.md)

Unabhängig vom verwendeten Stil müssen Sie ein serialisierungshandle erstellen, die Daten serialisieren und dann das Handle freigeben. Der Stil wird festgelegt, wenn das Programm das Handle erstellt und die Art und Weise definiert, wie ein Puffer manipuliert wird. Das Handle behält den entsprechenden Kontext bei, der jedem der drei serialisierungsstile zugeordnet ist.

 

 




