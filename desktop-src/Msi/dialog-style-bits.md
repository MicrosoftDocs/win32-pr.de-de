---
description: Der Stil eines Dialog Felds wird in der Spalte Attribute der Dialogfeld Tabelle durch ein 32-Bit-Wort angegeben, das aus stilbitflags besteht.
ms.assetid: aad719e8-86b3-4b2b-b417-db55013f8d3a
title: Dialog Feld stilbits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f22392ef9a88c547bd8fde5bc7df2f4839d66ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349321"
---
# <a name="dialog-style-bits"></a>Dialog Feld stilbits

Der Stil eines Dialog Felds wird in der Spalte Attribute der [Dialogfeld Tabelle](dialog-table.md) durch ein 32-Bit-Wort angegeben, das aus stilbitflags besteht.

In der folgenden Liste finden Sie Links zu Beschreibungen von reservierten Dialogfeld-Bits.



| Name                                                      | Decimal | Hexadezimal | Konstante                                                                                                                                       |
|-----------------------------------------------------------|---------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visible](visible-dialog-style-bit.md)                   | 1       | 0x00000001  | **msidbdialogattributesvisible**                                                                                                               |
| [Modal](modal-dialog-style-bit.md)                       | 2       | 0x00000002  | **msidbdialogattributesmodal**                                                                                                                 |
| [Minimieren](minimize-dialog-style-bit.md)                 | 4       | 0x00000004  | **msidbdialogattributesminimi**                                                                                                              |
| [Sysmodal](sysmodal-dialog-style-bit.md)                 | 8       | 0x00000008  | **msidbdialogattributessysmodal**                                                                                                              |
| [Keepmodeless](keepmodeless-dialog-style-bit.md)         | 16      | 0x00000010  | **msidbdialogattributeskeepmodeless**                                                                                                          |
| [Trackdiskspace](trackdiskspace-dialog-style-bit.md)     | 32      | 0x00000020  | **msidbdialogattributestrackdiskspace**                                                                                                        |
| [Usecustompalette](usecustompalette-dialog-style-bit.md) | 64      | 0x00000040  | **msidbdialogattributesusecustompalette**                                                                                                      |
| [Rtlro](rtlro-dialog-style-bit.md)                       | 128     | 0x00000080  | **msidbdialogattributesrtlro**                                                                                                                 |
| [Rechtsbündig](rightaligned-dialog-style-bit.md)         | 256     | 0x00000100  | **msidbdialogattributesrightausgerichteten**                                                                                                          |
| [Leftscroll](leftscroll-dialog-style-bit.md)             | 512     | 0x00000200  | **msidbdialogattributesleftscroll**                                                                                                            |
| [Bidi](bidi-dialog-style-bit.md)                         | 896     | 0x00000380  | **msidbdialogattributesbidi**  =  **msidbdialogattributesrtlro** \| **msidbdialogattributesrightausgerichteten** \| **msidbdialogattributesleftscroll** |
| [Fehler](error-dialog-style-bit.md)                       | 65536   | 0x00010000  | **msidbdialogattributeserror**                                                                                                                 |



 

 

 



