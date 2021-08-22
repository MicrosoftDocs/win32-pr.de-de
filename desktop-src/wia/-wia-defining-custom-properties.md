---
description: Definieren von benutzerdefinierten Eigenschaften.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definieren benutzerdefinierter Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b78516913c898e3b3d814e96a40d227cc3cc1cc70c13a290949f91eb9f447c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348050"
---
# <a name="defining-custom-properties"></a>Definieren benutzerdefinierter Eigenschaften

**Definieren benutzerdefinierter Eigenschaften**.

Wenn der WIA-Minitreiber (Windows Image Acquisition) benutzerdefinierte Eigenschaften definieren muss, sollte die WIA PRIVATE DEVPROP-Eigenschaft für benutzerdefinierte Stammelementeigenschaften und die \_ \_ WIA \_ PRIVATE ITEMPROP"-Eigenschaft für andere Elementeigenschaften verwendet \_ werden. Diese Konstanten werden in *wiadef.h definiert.*

Der folgende Beispielcode zeigt Definitionen für drei Stammelementeigenschaften. Die Eigenschaften-ID für die erste benutzerdefinierte Stammelementeigenschaft, CUSTOM ROOT PROP 1, wird in Bezug \_ \_ auf \_ WIA PRIVATE \_ \_ DEVPROP definiert. Eigenschaften-IDs für zusätzliche Stammelementeigenschaften werden in Bezug auf WIA \_ PRIVATE \_ DEVPROP + 1, WIA \_ PRIVATE \_ DEVPROP + 2 und so weiter definiert. Das Muster kann fortgesetzt werden, wenn zusätzliche benutzerdefinierte Stammelementeigenschaften erforderlich sind.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



Das nächste Beispiel zeigt Definitionen für drei benutzerdefinierte untergeordnete Elementeigenschaften und Eigenschaften-IDs. Die Eigenschaften-ID für die erste benutzerdefinierte untergeordnete Elementeigenschaft, CUSTOM CHILD PROP 1, wird in Bezug \_ \_ auf \_ WIA PRIVATE \_ \_ ITEMPROP definiert. Eigenschaften-IDs für zusätzliche untergeordnete Elementeigenschaften werden in Bezug auf WIA \_ PRIVATE \_ ITEMPROP + 1 definiert, und so weiter. Wie zuvor kann das Muster fortgesetzt werden, wenn weitere dieser benutzerdefinierten untergeordneten Elementeigenschaften erforderlich sind.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Benutzerdefinierte WIA-Eigenschaften müssen benutzerdefinierte Eigenschaftennamen aufweisen, die den benutzerdefinierten Eigenschaften-IDs zugeordnet sind. Der folgende Beispielcode zeigt Definitionen für drei benutzerdefinierte Stammelementeigenschaftsnamen. (Diese Eigenschaftennamen werden mit den benutzerdefinierten Eigenschaften-IDs verwendet, die in einem vorherigen Beispiel erstellt wurden, wobei der benutzerdefinierte Eigenschaftsname in CUSTOM enthalten ist. \_ ROOT \_ PROP \_ 1 STR ist der \_ benutzerdefinierten Stammelementeigenschafts-ID CUSTOM \_ ROOT PROP \_ \_ 1 zugeordnet.)


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> WIA-Eigenschaftennamen *werden nicht* in mehreren Sprachen lokalisiert. Dies liegt daran, dass WIA-Eigenschaften von Anwendungen mithilfe der Eigenschaften-ID oder des Eigenschaftennamens gelesen werden können. Wenn der Name verwendet wird, muss er eine Konstante sein, genau wie die Eigenschaften-ID.

 

 

 



