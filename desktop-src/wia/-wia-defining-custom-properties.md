---
description: Definieren von benutzerdefinierten Eigenschaften.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definieren von benutzerdefinierten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347598"
---
# <a name="defining-custom-properties"></a>Definieren von benutzerdefinierten Eigenschaften

**Definieren von benutzerdefinierten Eigenschaften**.

Wenn es erforderlich ist, dass der Windows-Abbild Erfassungs Dienst (WIA) benutzerdefinierte Eigenschaften definiert, sollte die WIA \_ private \_ devprop-Eigenschaft für benutzerdefinierte Stamm Element Eigenschaften verwendet werden, und die WIA \_ private \_ ItemProp-Eigenschaft sollte für andere Element Eigenschaften verwendet werden. Diese Konstanten werden in *wiadef. h* definiert.

Der folgende Beispielcode zeigt Definitionen für drei Stamm Element Eigenschaften. Die Eigenschaften-ID für die erste benutzerdefinierte root-Element Eigenschaft, die benutzerdefinierte Stamm-Prop-Eigenschaft \_ \_ \_ 1, wird in Form von WIA \_ private \_ devprop definiert. Eigenschaften-IDs für zusätzliche Stamm Element Eigenschaften werden in Form von WIA \_ private \_ devprop + 1, WIA \_ private \_ devprop + 2 usw. definiert. Das Muster kann fortgesetzt werden, wenn zusätzliche benutzerdefinierte Stamm Element Eigenschaften benötigt werden.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



Das nächste Beispiel zeigt Definitionen für drei benutzerdefinierte untergeordnete Element Eigenschaften und Eigenschaften-IDs. Die Eigenschaften-ID für die erste benutzerdefinierte untergeordnete Element Eigenschaft, benutzerdefinierte untergeordnete \_ \_ Prop \_ 1, wird in Form von WIA \_ private \_ ItemProp definiert. Eigenschaften-IDs für zusätzliche untergeordnete Element Eigenschaften werden in Form von WIA \_ private \_ ItemProp + 1 usw. definiert. Wie zuvor kann das Muster fortgesetzt werden, wenn mehr dieser Eigenschaften für ein benutzerdefiniertes untergeordnetes Element benötigt wird.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Benutzerdefinierte WIA-Eigenschaften müssen benutzerdefinierte Eigenschaftsnamen aufweisen, die den benutzerdefinierten Eigenschaften-IDs zugeordnet sind. Der folgende Beispielcode zeigt Definitionen für drei benutzerdefinierte Stamm Element-Eigenschaften Namen. (Diese Eigenschaftsnamen werden mit den benutzerdefinierten Eigenschaften-IDs verwendet, die in einem vorherigen Beispiel erstellt wurden, wobei der Name der benutzerdefinierten Eigenschaft in Custom \_ Root \_ Prop \_ 1 \_ str ist der benutzerdefinierten Stamm-ID des Stamm Elements \_ root \_ Prop \_ 1 zugeordnet.)


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> WIA-Eigenschaften Namen sind in mehreren Sprachen *nicht* lokalisiert. Dies liegt daran, dass WIA-Eigenschaften von Anwendungen gelesen werden können, die die Eigenschaften-ID oder den Eigenschaften Namen verwenden. Wenn der Name verwendet wird, muss er eine Konstante sein, ebenso wie die eigen schafts-ID.

 

 

 



