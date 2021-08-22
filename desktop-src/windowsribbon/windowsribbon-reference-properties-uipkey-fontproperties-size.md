---
title: UI_PKEY_FontProperties_Size
description: Identifiziert die \_ PKEY \_ FontProperties \_ Size-Eigenschaft der Benutzeroberfläche.
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c013c41290f6e062b03572a9e3cb848752efcb12f1c779348a0253f94d40e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028628"
---
# <a name="ui_pkey_fontproperties_size"></a>UI \_ PKEY \_ FontProperties \_ Size

Identifiziert die \_ PKEY \_ FontProperties \_ Size-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Hinweise

Ui PKEY FontProperties Size wird von einer Anwendung verwendet, um den Wert des Steuerelements \_ \_ \_ **Schriftgrad abfragt.**

Gültige Werte für diese Eigenschaft reichen von 1 bis einschließlich 9999. Wenn ein Benutzer versucht, einen ungültigen Wert eineingaben, wird der Eintrag abgelehnt, und das Steuerelement Schriftgrad wird auf den letzten gültigen Wert zurückverwendet. 

Wenn eine Anwendung versucht, den Schriftgrad programmgesteuert auf einen Wert außerhalb des gültigen Bereichs zu setzen, macht das Menübandframework alle Schriftarteigenschaften ungültig und legt die Schriftartsteuerelemente **(** Schriftgrad und Schriftartgesicht **)** auf leer oder gegebenenfalls auf ihren Standardzustand fest.

Der Standardwert ist 0.

Der Wert 0 gibt an, dass keine Einzelpunktgröße ausgewählt wird (es wird entweder kein Text oder eine Ausführung mit heterogenem Text ausgewählt).

Ein Benutzer kann das Steuerelement **Schriftgrad nicht** auf 0 festlegen.

Ab dem Wert 0 liegen gültige Werte für \_ ui PKEY \_ FontProperties Size zwischen \_ *MinimumFontSize* und *MaximumFontSize,* wie im [Font Control-Markup](windowsribbon-controls-fontcontrol.md) deklariert.

> [!Note]  
> Das **Steuerelement Schriftgrad** wird auf leer festgelegt, wenn der Schriftgrad programmgesteuert auf 0 festgelegt ist, z. B. wenn eine Ausführung von heterogenem Text hervorgehoben ist.

 

Wenn eine Ausführung von heterogenem Text ausgewählt ist, sollte die Anwendung [ \_ PKEY \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) der Benutzeroberfläche abfragen, um die Befehle **Schriftart** vergrößeren und **Schriftart verkleinern zu** erfassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




