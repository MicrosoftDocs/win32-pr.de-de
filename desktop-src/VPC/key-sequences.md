---
title: Schlüsselsequenzen
description: Eine Schlüssel Sequenz Zeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüssel Bezeichnerzeichen, die verwendet werden, um die Tastenkombination und die releasesequenz einer Standardtastatur des US-amerikanischen 101-Schlüssels zu simulieren.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Virtueller Computer für Windows Virtual PC, schlüsselsequenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c973b5aafd3bf02746ac1550ffedf3d4a4c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729281"
---
# <a name="key-sequences"></a>Schlüsselsequenzen

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Eine Schlüssel Sequenz Zeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüssel Bezeichnerzeichen, die verwendet werden, um die Tastenkombination und die releasesequenz einer Standardtastatur des US-amerikanischen 101-Schlüssels zu simulieren.

Wenn ein Schlüssel Bezeichner in der Zeichenfolge ohne einen vorangehenden Modifizierer angezeigt wird, wird ein Schlüssel gesteuertes Code simuliert, gefolgt vom zugehörigen Code, der durch den Schlüssel freigegeben wurde. Schlüsselmodifizierer können verwendet werden, um dieses Verhalten zu ändern.

Der **down** -Modifizierer sendet z. b. den Schlüssel gesteuerten Code für den folgenden Schlüssel Bezeichner, ohne den Schlüssel freigegebenen Code zu senden. Dies ist nützlich zum Simulieren von STRG-, alt-und Umschalttaste, wenn Sie gedrückt werden, während andere Schlüssel gesendet werden. Um den Schlüssel freizugeben, muss er erneut in die Schlüssel Zeichenfolge eingefügt werden, zusammen mit **einem vorangehenden** Modifizierer.

## <a name="key-identifiers"></a>Schlüssel Bezeichner

Die folgende Liste enthält die gültigen schlüsselbezeichnerzeichenfolgen. 

| Key Identifier-Zeichenfolge | Bedeutung                         |
|-----------------------|---------------------------------|
| Key- \_ Escape           | **ESC** -Taste                 |
| Schlüssel \_ F1               | **F1** -Taste                  |
| Schlüssel \_ F2               | **F2** -Taste                  |
| Taste \_ F3               | **F3** -Taste                  |
| Schlüssel \_ F4               | **F4** -Taste                  |
| Taste \_ F5               | **F5** -Taste                  |
| Schlüssel \_ F6               | **F6** -Taste                  |
| Schlüssel \_ F7               | **F7** -Taste                  |
| Schlüssel \_ F8               | **F8** -Taste                  |
| Schlüssel \_ F9               | **F9** -Taste                  |
| Taste \_ F10              | **F10** -Taste                 |
| Taste \_ F11              | **F11** -Taste                 |
| Taste \_ F12              | **F12** -Taste                 |
| Schlüssel- \_ sysreq           | der **sysreq** -Schlüssel              |
| Key \_ ScrollLock       | **ScrollLock** -Taste          |
| Schlüssel \_ Umbruch            | **Pause** -Taste               |
| Schlüssel \_ leftapostroph   | der **\`** Schlüssel                  |
| Schlüssel \_ 1                | **1** -Taste                   |
| Schlüssel \_ 2                | **2** -Taste                   |
| Schlüssel \_ 3                | **3** -Taste                   |
| Schlüssel \_ 4                | **4** -Taste                   |
| Schlüssel \_ 5                | **5** -Taste                   |
| Schlüssel \_ 6                | **6** -Taste                   |
| Schlüssel \_ 7                | **7** -Taste                   |
| Schlüssel \_ 8                | **8** -Taste                   |
| Schlüssel \_ 9                | **9** -Taste                   |
| Schlüssel \_ 0                | **0** -Taste                   |
| Key- \_ Bindestrich           | der **-** Schlüssel                   |
| Schlüssel ist \_ Gleichheits           | der **=** Schlüssel                   |
| Schlüssel \_ RÜCKTASTE        | **RÜCKTASTE**           |
| Key \_ Insert           | die **ins** -Taste                 |
| Key \_ Home             | der **Home** -Schlüssel                |
| \_Schlüsselpageup           | die **PageUp** -Taste              |
| Schlüssel- \_ Numlock          | **Numlock** -Schlüssel             |
| Unterteilung von Keypad \_        | der **/** Schlüssel auf der Tastatur     |
| Tastenkombination \_      | der **\*** Schlüssel auf der Tastatur    |
| Keypad \_ minus         | der **-** Schlüssel auf der Tastatur     |
| Schlüssel \_ Registerkarte              | **Tab** -Taste                 |
| Key \_ Q                | **Q** -Taste                   |
| Schlüssel \_ W                | **W** -Taste                   |
| Schlüssel \_ E                | **E** -Taste                   |
| Schlüssel \_ R                | **R** -Taste                   |
| Schlüssel \_ T                | **T** -Taste                   |
| Schlüssel \_ Y                | **Y** -Taste                   |
| Schlüssel \_ U                | **U** -Taste                   |
| Schlüssel \_ I                | die **I** -Taste                   |
| Key \_ O                | **O** -Taste                   |
| Key \_ P                | **P** -Taste                   |
| Schlüssel \_ leftklammer      | der **\[** Schlüssel                  |
| Key \_ rightklammer     | der **\]** Schlüssel                  |
| Umgekehrter \_ Schrägstrich        | der **\\** Schlüssel                  |
| Schlüssel \_ Löschen           | die  ENTF-Taste              |
| Schlüssel \_ Ende              | die **endtaste**                 |
| Schlüssel \_ PageDown         | die **PageDown** -Taste            |
| Keypad \_ 7             | **7** -Taste auf der Tastatur     |
| Tastatur \_ 8             | **8** -Taste auf der Tastatur     |
| Keypad \_ 9             | **9** -Taste auf der Tastatur     |
| Keypad \_ Plus          | der **+** Schlüssel auf der Tastatur     |
| Schlüssel \_ A                | die **A** -Taste                   |
| Schlüssel \_ S                | die **S** -Taste                   |
| Schlüssel \_ D                | **D-** Taste                   |
| Key \_ F                | **F** -Taste                   |
| Key \_ G                | **G** -Taste                   |
| Schlüssel \_ H                | **H** -Taste                   |
| Schlüssel \_ J                | **J** -Taste                   |
| Schlüssel \_ K                | **K** -Taste                   |
| Schlüssel \_ L                | **L** -Taste                   |
| Schlüssel \_ Semikolon        | die **Schlüssel**                   |
| Schlüssel- \_ singleanführungs Zeichen      | der **Schlüssel**                   |
| Schlüssel \_ Eingabe            | **Eingabe** Taste               |
| Keypad \_ 4             | **4** -Taste auf der Tastatur     |
| Keypad \_ 5             | **5** -Taste auf der Tastatur     |
| Keypad \_ 6             | **6** -Taste auf der Tastatur     |
| Schlüssel \_ LeftShift        | **linke UMSCHALT** Taste          |
| Schlüssel \_ Z                | **Z** -Taste                   |
| Schlüssel \_ X                | **X** -Taste                   |
| Schlüssel \_ C                | **C** -Taste                   |
| Schlüssel \_ V                | **V** -Taste                   |
| Schlüssel \_ B                | **B** -Taste                   |
| Schlüssel \_ N                | **N** -Taste                   |
| Schlüssel \_ M                | **M** -Taste                   |
| Schlüssel \_ Komma            | **,** Schlüssel                   |
| Schlüssel \_ Zeitraum           | die **.** Schlüssel                   |
| Schlüssel \_ Schrägstrich            | der **/** Schlüssel                   |
| Key- \_ RightShift       | **Rechte UMSCHALT** Taste         |
| Schlüssel \_ aufwärts               | nach- **oben** -Taste                  |
| Keypad \_ 1             | **1** -Taste auf der Tastatur     |
| Tastatur \_ 2             | **2** -Taste auf der Tastatur     |
| Keypad \_ 3             | **3** -Taste auf der Tastatur     |
| Tastatur \_ EINGABETASTE         | **Eingabe** Taste auf der Tastatur |
| Schlüssel \_ leftctrl         | **linke STRG** -Taste           |
| Key \_ leftwindows      | **linke Windows** -Taste        |
| Key \_ LeftAlt          | **linke alt** -Taste            |
| Schlüssel \_ Bereich            | die **LEERTASTE**               |
| Key \_ rightalt         | die **Rechte alt** -Taste           |
| Key \_ rightwindows     | die **Rechte Windows** -Taste       |
| Schlüssel \_ Rechts STRG        | die **Rechte STRG** -Taste          |
| Schlüssel \_ Anwendung      | **Anwendungs** Schlüssel         |
| Schlüssel \_ Links             | die **linke** Taste                |
| Taste \_ unten             | **nach-unten** -Taste                |
| Schlüssel \_ Rechts            | **rechter** Schlüssel               |
| Keypad \_ 0             | **0** -Taste auf der Tastatur     |
| Keypad- \_ decimalpoint  | die **.** Schlüssel auf der Tastatur     |



 

## <a name="key-modifiers"></a>Schlüsselmodifizierer

Die folgende Liste enthält die gültigen schlüsselmodifiziererzeichenfolgen. 

| Schlüsselmodifizierer Zeichenfolge | Bedeutung                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| DOWN                | Senden Sie einen Schlüssel gesteuerten Code für den folgenden Schlüssel Bezeichner, ohne einen Schlüssel freigegebenen Code zu senden. |
| UP                  | Senden Sie einen Schlüssel freigegebenen Code für den folgenden Schlüssel Bezeichner.                                    |
| HOLD                | Halten Sie 200 Millisekunden an, bevor Sie die Verarbeitung der restlichen Schlüssel Sequenz Zeichenfolge fortsetzen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ivmkeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 