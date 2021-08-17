---
title: Serialisierungsstile
description: Es gibt drei Stile, mit denen Sie Serialisierungshandles bearbeiten können.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfaa7cd3198245441a27990d331bcd9f0bd0396b5075d9985b13da58012147d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925386"
---
# <a name="serialization-styles"></a>Serialisierungsstile

Es gibt drei Stile, mit denen Sie Serialisierungshandles bearbeiten können. Diese lauten wie folgt:

-   [Feste Pufferserialisierung](fixed-buffer-serialization.md)
-   [Dynamische Pufferserialisierung](dynamic-buffer-serialization.md)
-   [Inkrementelle Serialisierung](incremental-serialization.md)

Unabhängig vom verwendeten Stil müssen Sie ein Serialisierungshandle erstellen, die Daten serialisieren und dann das Handle freigeben. Der Stil wird festgelegt, wenn das Programm das Handle erstellt und die Art und Weise definiert, wie ein Puffer bearbeitet wird. Das Handle behält den entsprechenden Kontext bei, der jedem der drei Serialisierungsstile zugeordnet ist.

 

 




