---
title: UI_PKEY_FontProperties_Size
description: Gibt die Größe der Eigenschaft "UI- \_ pkey \_ fontproperties" an \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339791"
---
# <a name="ui_pkey_fontproperties_size"></a>Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_

Gibt die Größe der Eigenschaft "UI- \_ pkey \_ fontproperties" an \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Bemerkungen

\_Die Größe der UI-pkey- \_ fontproperties \_ wird von einer Anwendung verwendet, um den Wert des Steuer Elements für die **Schriftgröße** abzufragen.

Gültige Werte für diese Eigenschaft liegen zwischen 1 und 9999 (einschließlich). Wenn ein Benutzer versucht, einen ungültigen Wert einzugeben, wird der Eintrag abgelehnt, und das **Schriftart Größen** Steuerelement wird auf den letzten gültigen Wert zurückgesetzt.

Wenn eine Anwendung versucht, die Schriftgröße Programm gesteuert auf einen Wert außerhalb des gültigen Bereichs festzulegen, werden alle Schriftart Eigenschaften für das Menüband-Framework ungültig und die Schriftart Steuerelemente (**Schrift** Grad und **Schriftart**) auf leer oder auf ihren Standardzustand (soweit zutreffend) festgelegt.

Der Standardwert ist 0.

Der Wert 0 gibt an, dass keine einzelne Punktgröße ausgewählt ist (entweder kein Text oder eine ausgewertegröße mit Hetero gener Größe).

Ein Benutzer kann das Steuerelement für die **Schriftgröße** nicht auf 0 festlegen.

Ein anderer Wert als 0 gibt an, dass gültige Werte für \_ \_ die Eigenschaften der UI-pkey-fontproperties \_ zwischen *MinimumFontSize* und *maximumfontsize* liegen, wie im [Schriftart-Steuer](windowsribbon-controls-fontcontrol.md) Element Markup deklariert.

> [!Note]  
> Das **Schriftart Größe** -Steuerelement wird auf leer festgelegt, wenn der Schrift Grad Programm gesteuert auf 0 festgelegt ist, z. b. Wenn ein Text mit einer heterogenen Größe hervorgehoben wird.

 

Wenn ein Text mit heterogener Größe ausgewählt wird, muss die Anwendung die [UI \_ pkey \_ fontproperties \_ Delta size](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) Abfragen, um die Befehle zum **vergrößern Schriftart** und zum **Verkleinern der Schriftart** zu erfassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




