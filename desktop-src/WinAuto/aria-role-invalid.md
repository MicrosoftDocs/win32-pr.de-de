---
title: ARIA-Rollenfehler
description: ARIA-Rollenfehler
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134013"
---
# <a name="aria-role-error"></a>ARIA-Rollenfehler

## <a name="text"></a>Text

Das Element verfügt über eine ungültige MSI-ARIA-Rolle.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für alle [](https://developer.mozilla.org/docs/Web/HTML/Reference) Elemente, die über das Rollenattribut verfügen. Es gibt an, dass es sich bei dem **Rollenattribut** nicht um einen gültigen Rollenwert der Initiative für webbarrierefreiheit – barrierefreie Rich Internet Applications (WLAN-ARIA) handelt, wie in der SPEZIFIKATION DER ARIA-Spezifikation definiert. Durch das Festlegen einer gültigen Rolle wird sichergestellt, dass das Element von Sprachausgaben und anderen Hilfstechnologietools ordnungsgemäß interpretiert wird.

Um diesen Fehler zu [](https://developer.mozilla.org/docs/Web/HTML/Reference) beheben, legen Sie das Rollenattribut auf einen gültigen ATTRIBUT-ARIA-Rollenwert fest. Beachten Sie, dass abstrakte CAB-ARIA-Rollen ungültig sind.

## <a name="example"></a>Beispiel


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ARIA-Containerrollenfehler](aria-container-role.md)
</dt> </dl>

 

 




