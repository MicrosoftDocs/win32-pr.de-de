---
title: Aria-TabIndex-Fehler
description: Aria-TabIndex-Fehler
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- Ariatabindexerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039779"
---
# <a name="aria-tabindex-error"></a>Aria-TabIndex-Fehler

## <a name="text"></a>Text

Das Element ist nicht deaktiviert und verfügt über einen **Click** -Ereignishandler, verfügt jedoch über **TabIndex** < 0 und ist nicht standardmäßig in der Aktivier Reihenfolge.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die einen Click-Ereignishandler haben und nicht deaktiviert sind. Diese Elemente müssen sich in der Aktivier Reihenfolge befinden. Dadurch wird sichergestellt, dass ein Element mithilfe der Tab-Taste erreicht werden kann. auf diese Weise navigieren Benutzer in der Benutzeroberfläche.

Legen Sie zum Beheben dieses Fehlers das [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) -Attribut auf einen Wert fest, der größer oder gleich 0 (null) ist. Sie müssen das **TabIndex** -Attribut nicht explizit für Tags festlegen, die sich standardmäßig in der Aktivier Reihenfolge befinden, z. b [**. (mit**](https://developer.mozilla.org/docs/Web/HTML/Element/a) [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) -Attribut), [**Schaltfläche**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**Eingabe**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (mit Ausnahme von "Hidden"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**Textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)und [**Area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (als Teil der ImageMap).

## <a name="example"></a>Beispiel


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




