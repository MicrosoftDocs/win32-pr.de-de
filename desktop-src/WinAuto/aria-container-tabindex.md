---
title: TabIndex-Fehler bei Aria-Container
description: TabIndex-Fehler bei Aria-Container
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- Ariacontainertabindexerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388674"
---
# <a name="aria-container-tabindex-error"></a>TabIndex-Fehler bei Aria-Container

## <a name="text"></a>Text

Das-Element ist ein Fokus nutzbarer Container mit aktiven, aber ohne **TabIndex** -Wert größer oder gleich 0.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für-Elemente, die über das **Aria-activenachfolger** -Attribut verfügen, nicht deaktiviert sind und das **TabIndex** -Attribut nicht auf einen Wert festgelegt ist, der größer oder gleich 0 (null) ist. Diese Elemente müssen sich in der Aktivier Reihenfolge befinden, da Sie für die Verarbeitung von Tastatur Ereignissen für ihre untergeordneten Elemente zuständig sind

Legen Sie zum Beheben dieses Fehlers das **TabIndex** -Attribut auf einen Wert fest, der größer oder gleich 0 (null) ist.

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

[TabIndex Fehler bei der Aria-Container Rolle (ohne aktiven Nachfolger)](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




