---
title: Aria-Rollen Fehler
description: Aria-Rollen Fehler
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- Ariaroleerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106341337"
---
# <a name="aria-role-error"></a>Aria-Rollen Fehler

## <a name="text"></a>Text

Das Element hat eine ungültige WAI-ARIA-Rolle.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für alle Elemente, die über das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut verfügen. Der Wert gibt an, dass das **Role** -Attribut kein gültiger Rollen Wert für die webobarrierefreiheits Initiative ist, der von der WAI-ARIA-Spezifikation definiert wurde. Durch Festlegen einer gültigen Rolle wird sichergestellt, dass das Element von sprach Lesern und anderen hilfstechnologietools richtig interpretiert wird.

Legen Sie zum Beheben dieses Fehlers das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut auf einen gültigen Wert der Rolle "WAI-ARIA" fest. Beachten Sie, dass abstrakte WAI-ARIA-Rollen nicht gültig sind.

## <a name="example"></a>Beispiel


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler bei der Aria-Container Rolle](aria-container-role.md)
</dt> </dl>

 

 




