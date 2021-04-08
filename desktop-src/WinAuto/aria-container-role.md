---
title: Fehler bei der Aria-Container Rolle
description: Fehler bei der Aria-Container Rolle
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- Ariacontainerroleerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948024"
---
# <a name="aria-container-role-error"></a>Fehler bei der Aria-Container Rolle

## <a name="text"></a>Text

Das Element, für das " **Active-** Nachfolger" definiert ist, besitzt keine Container Rolle (**ComboBox**, **Grid**, **ListBox**, **Menu**, **Menüleiste**, **Radio Group**, **Tree**, **treegrid**, **TabList**, **Row**).

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für-Elemente, die über das **Aria-activenachfolger** -Attribut verfügen.

Ein Element scheint ein Container zu sein, für den das Attribut " **Aria-activenachfolger** " festgelegt ist, aber das Rollen Attribut des Elements hat keinen Wert, der für einen Container gültig ist.

Um diesen Fehler zu beheben, legen Sie das **Role** -Attribut auf eine webressbarrierefreiheits-Initiative zugreifen, auf die der Rollen Wert "Ria-Aria" zugreifen kann, der für ein Containerelement gültig ist: **ComboBox**, **Grid**, **ListBox**, **Menu**, **Menüleiste**, **Radio Group**, **TabList**, **Tree** oder **treegrid**.

## <a name="example"></a>Beispiel


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aria-Rollen Fehler](aria-role-invalid.md)
</dt> </dl>

 

 




