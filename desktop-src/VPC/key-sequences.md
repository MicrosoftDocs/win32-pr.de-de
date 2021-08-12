---
title: Schlüsselsequenzen
description: Eine Tastensequenzzeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüsselbezeichnern, die verwendet werden, um die Tastenkombination und die Freigabesequenz einer STANDARDTASTATUR (U.S. 101) zu simulieren.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Windows Virtueller PC , Tastensequenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b300c1d417bad30f7a0e06fd8cfb411184eb8f6b800549536c9b6452dcdfefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591445"
---
# <a name="key-sequences"></a>Schlüsselsequenzen

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Eine Tastensequenzzeichenfolge ist ein durch Trennzeichen getrennter Satz von Schlüsselbezeichnern, die verwendet werden, um die Tastenkombination und die Freigabesequenz einer STANDARDTASTATUR (U.S. 101) zu simulieren.

Wenn ein Schlüsselbezeichner in der Zeichenfolge ohne vorangehenden Modifizierer angezeigt wird, wird ein per Taste gedrückter Code simuliert, unmittelbar gefolgt von dem entsprechenden, von der Taste freigegebenen Code. Schlüsselmodifizierer können verwendet werden, um dieses Verhalten zu ändern.

Der DOWN-Modifizierer sendet z. B. den gedrückten Code für den folgenden Schlüsselbezeichner, ohne den code freigelassenen Schlüssel zu senden.  Dies ist nützlich, um STRG-, ALT- und UMSCHALTTASTEn zu simulieren, wenn sie gedrückt gehalten werden, während andere Tasten gesendet werden. Um den Schlüssel frei zu geben, muss er zusammen mit einem vorangehenden UP-Modifizierer erneut in die **Schlüsselzeichenfolge eingeschlossen** werden.

## <a name="key-identifiers"></a>Schlüsselbezeichner

In der folgenden Liste sind die gültigen Schlüsselbezeichnerzeichenfolgen aufgeführt. 

| Schlüsselbezeichnerzeichenfolge | Bedeutung                         |
|-----------------------|---------------------------------|
| Key \_ Escape           | **ESC-TASTE**                 |
| Taste \_ F1               | **F1-TASTE**                  |
| Taste \_ F2               | **F2-TASTE**                  |
| Taste \_ F3               | **F3-TASTE**                  |
| Taste \_ F4               | **F4-TASTE**                  |
| Taste \_ F5               | **F5-TASTE**                  |
| Taste \_ F6               | **F6-TASTE**                  |
| Taste \_ F7               | **F7-TASTE**                  |
| Taste \_ F8               | **F8-TASTE**                  |
| Taste \_ F9               | **F9-TASTE**                  |
| Taste \_ F10              | **F10-TASTE**                 |
| Taste \_ F11              | **F11-TASTE**                 |
| Taste \_ F12              | **F12-TASTE**                 |
| \_SysReq-Schlüssel           | **SysReq-Schlüssel**              |
| Key \_ ScrollLock       | **ScrollLock-Taste**          |
| Key \_ Break            | Die **Break-TASTE**               |
| Schlüssel \_ linksApostrophe   | den **\`** Schlüssel                  |
| Schlüssel \_ 1                | **1-Taste**                   |
| Schlüssel \_ 2                | die **2-Taste**                   |
| Schlüssel \_ 3                | die **3-Taste**                   |
| Schlüssel \_ 4                | die **4-Taste**                   |
| Schlüssel \_ 5                | die **5-Taste**                   |
| Schlüssel \_ 6                | die **6-Taste**                   |
| Schlüssel \_ 7                | die **7-Taste**                   |
| Schlüssel \_ 8                | 8 **Schlüssel**                   |
| Schlüssel \_ 9                | die **9-Taste**                   |
| Schlüssel \_ 0                | **0-Taste**                   |
| Schlüssel \_ bindestrich           | den **-** Schlüssel                   |
| \_Schlüsselgleichheit           | den **=** Schlüssel                   |
| Key \_ Backspace        | Die **Rücktaste**           |
| \_Schlüsseleinfügung           | **Ins-Taste**                 |
| Key \_ Home             | Den **Schlüssel "Home"**                |
| Key \_ PageUp           | **PageUp-Schlüssel**              |
| Key \_ NumLock          | **NumLock-Taste**             |
| KeyPad \_ Divide        | Die **/** Taste auf der Tastatur     |
| Multiplizieren des \_ KeyPads      | Die **\*** Taste auf der Tastatur    |
| KeyPad \_ Minus         | Die **-** Taste auf der Tastatur     |
| Registerkarte \_ "Schlüssel"              | **TAB-TASTE**                 |
| Schlüssel \_ Q                | **Q-Taste**                   |
| Schlüssel \_ W                | **W-Taste**                   |
| Schlüssel \_ E                | **E-Taste**                   |
| Schlüssel \_ R                | **R-Taste**                   |
| Schlüssel \_ T                | **T-Taste**                   |
| Schlüssel \_ Y                | **Y-Taste**                   |
| Schlüssel \_ U                | **U-Taste**                   |
| Schlüssel \_ I                | **I-Taste**                   |
| Schlüssel \_ O                | **O-Schlüssel**                   |
| Schlüssel \_ P                | **P-Taste**                   |
| Key \_ LeftBracket      | der **\[** Schlüssel                  |
| Key \_ RightBracket     | der **\]** Schlüssel                  |
| Umgekehrter \_ Schrägstrich        | der **\\** Schlüssel                  |
| \_Schlüssellöschung           | Der **Löschschlüssel**              |
| \_Schlüsselende              | **Der Endschlüssel**                 |
| Key \_ PageDown         | **PageDown-Taste**            |
| KeyPad \_ 7             | die **7-Taste** auf der Tastatur     |
| KeyPad \_ 8             | die **8-Taste** auf der Tastatur     |
| KeyPad \_ 9             | Die **9-Taste** auf der Tastatur     |
| KeyPad \_ Plus          | **+** die Taste auf der Tastatur     |
| Schlüssel \_ A                | **A-Schlüssel**                   |
| Schlüssel \_ S                | **S-Taste**                   |
| Schlüssel \_ D                | **D-Taste**                   |
| Taste \_ F                | **F-TASTE**                   |
| Schlüssel \_ G                | **G-Taste**                   |
| Schlüssel \_ H                | **H-Taste**                   |
| Schlüssel \_ J                | **J-Schlüssel**                   |
| Schlüssel \_ K                | **K-Taste**                   |
| Schlüssel \_ L                | **L-Taste**                   |
| \_Schlüssel-Semikolon        | der **Schlüssel ;**                   |
| Key \_ SingleQuote      | Schlüssel **""**                   |
| \_EINGABETASTE            | **Die EINGABETASTE**               |
| KeyPad \_ 4             | die **4-Taste** auf der Tastatur     |
| KeyPad \_ 5             | **die 5-Taste** auf der Tastatur     |
| KeyPad \_ 6             | **6-Taste** auf der Tastatur     |
| Key \_ LeftShift        | **Umschalttaste nach links**          |
| Schlüssel \_ Z                | **Z-Taste**                   |
| Schlüssel \_ X                | **X-Taste**                   |
| Schlüssel \_ C                | **C-Taste**                   |
| Schlüssel \_ V                | der **V-Schlüssel**                   |
| Schlüssel \_ B                | **B-Taste**                   |
| Schlüssel \_ N                | **N-Taste**                   |
| Schlüssel \_ M                | **M-Taste**                   |
| \_Schlüssel-Komma            | der **Schlüssel ,**                   |
| \_Schlüsselzeitraum           | die **.** key                   |
| Schrägstrich \_ (Key Slash)            | der **/** Schlüssel                   |
| Key \_ RightShift       | **DIE UMSCHALTTASTE NACH RECHTS**         |
| Key \_ Up               | **Up-Taste**                  |
| KeyPad \_ 1             | **1** Taste auf der Tastatur     |
| KeyPad \_ 2             | die **2-Taste** auf der Tastatur     |
| KeyPad \_ 3             | die **3-Taste** auf der Tastatur     |
| \_KeyPad-EINGABETASTE         | **Die EINGABETASTE** auf der Tastatur |
| Key \_ LeftCtrl         | **DIE LINKE STRG-TASTE**           |
| Key \_ LeftWindows      | Die **linke Windows**        |
| Key \_ LeftAlt          | DIE **LINKE ALT-TASTE**            |
| \_Schlüsselbereich            | Der **Schlüssel "Space"**               |
| Key \_ RightAlt         | DIE **RECHTE ALT-TASTE**           |
| Key \_ RightWindows     | Rechter **Windows**       |
| Key \_ RightCtrl        | DIE **RECHTE STRG-TASTE**          |
| \_Schlüsselanwendung      | **Anwendungsschlüssel**         |
| Schlüssel \_ links             | Die **linke** Taste                |
| Key \_ Down             | DIE **TASTE "NACH UNTEN"**                |
| \_Schlüsselrecht            | Der **richtige** Schlüssel               |
| KeyPad \_ 0             | Die **0-Taste** auf der Tastatur     |
| KeyPad \_ DecimalPoint  | die **.** Taste auf der Tastatur     |



 

## <a name="key-modifiers"></a>Schlüsselmodifizierer

In der folgenden Liste sind die gültigen Schlüsselmodifiziererzeichenfolgen aufgeführt. 

| Schlüsselmodifiziererzeichenfolge | Bedeutung                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| DOWN                | Senden Sie einen durch die Taste gedrückten Code für den folgenden Schlüsselbezeichner, ohne einen von der Taste freigegebenen Code zu senden. |
| UP                  | Senden Sie einen schlüsselverknickten Code für den folgenden Schlüsselbezeichner.                                    |
| HOLD                | Halten Sie 200 Millisekunden an, bevor Sie den Rest der Schlüsselsequenzzeichenfolge verarbeiten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 