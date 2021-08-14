---
title: E (Menüs und andere Ressourcen)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f2423b002afe055c425978a643753e029d817eee5e7eccfc4379d2410f88ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461250"
---
# <a name="e-menus-and-other-resources"></a>E (Menüs und andere Ressourcen)

[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Leere Menüs nicht zulässig**
</dt> <dd>

Ein **END-Schlüsselwort** wird angezeigt, bevor Menüelemente in der [**MENU-Anweisung**](menu-resource.md) definiert werden. Leere Menüs sind vom Microsoft Windows 32 Resource Compiler (RC) nicht zulässig. Stellen Sie sicher, dass in der **MENU-Anweisung** keine öffnenden Anführungszeichen vorhanden sind.

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END im Dialogfeld erwartet**
</dt> <dd>

Das **END-Schlüsselwort** muss am Ende einer [**DIALOG-Anweisung**](dialog-resource.md) angezeigt werden. Stellen Sie sicher, dass von der vorherigen Anweisung keine öffnenden Anführungszeichen mehr vorhanden sind.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END im Menü erwartet**
</dt> <dd>

Das **END-Schlüsselwort** muss am Ende einer [**MENU-Anweisung**](menu-resource.md) angezeigt werden. Stellen Sie sicher, dass keine nicht übereinstimmenden **BEGIN-** und **END-Anweisungen** vorhanden sind.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Fehler beim Erstellen von Ressourcenname**
</dt> <dd>

Der Microsoft Windows 32-Ressourcencompiler (RC) konnte die angegebene binäre Ressource (. RES)-Datei. Stellen Sie sicher, dass sie nicht auf einem schreibgeschützten Laufwerk erstellt wird. Verwenden Sie die Option **/v,** um herauszufinden, ob die Datei erstellt wird.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Erwartetes Komma in der Zugriffstastentabelle**
</dt> <dd>

Microsoft Windows 32 Resource Compiler (RC) erfordert ein Komma zwischen den *Parametern event* und *idvalue* in der [**ACCELERATORS-Anweisung.**](accelerators-resource.md)

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Erwarteter Name der Steuerelementklasse**
</dt> <dd>

Der *Klassenparameter* einer [**CONTROL-Anweisung**](control-control.md) in der [**DIALOG-Anweisung**](dialog-resource.md) muss einer der folgenden Steuerelementtypen sein: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC** oder benutzerdefiniert. Stellen Sie sicher, dass die Klasse richtig geschrieben ist.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Erwarteter Schriftart-Gesichtsname**
</dt> <dd>

Der *Typeface-Parameter* der **FONT-Anweisung** in der [**DIALOG-Anweisung**](dialog-resource.md) muss eine Zeichenfolge sein, die in doppelte Anführungszeichen (") eingeschlossen ist. Dieser Parameter gibt den Namen einer Schriftart an.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Erwarteter ID-Wert für Menuitem**
</dt> <dd>

Die [**MENU-Anweisung**](menu-resource.md) muss eine [**MENUITEM-Anweisung**](menuitem-statement.md) enthalten, die entweder eine ganze Zahl oder eine symbolische Konstante im *MenuID-Parameter* enthält.

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Erwartete Menüzeichenfolge**
</dt> <dd>

Jede [**MENUITEM-**](menuitem-statement.md) und [**POPUP-Anweisung**](popup-resource.md) muss einen *Textparameter* enthalten. Dieser Parameter ist eine Zeichenfolge, die in doppelte Anführungszeichen (") eingeschlossen ist und den Namen des Menüelements oder Popupmenüs angibt. Eine **MENUITEM SEPARATOR-Anweisung** erfordert keine Zeichenfolge in Anführungszeichen.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Erwarteter numerischer Befehlswert**
</dt> <dd>

Microsoft Windows Resource Compiler (RC) hat einen numerischen *idvalue-Parameter* in der [**ACCELERATORS-Anweisung**](accelerators-resource.md) erwartet. Stellen Sie sicher, dass Sie eine [**\# define-Anweisung**](-define.md) verwendet haben, um den Wert anzugeben, und dass die verwendete Konstante richtig geschrieben ist.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Erwartete numerische Konstante in einer Zeichenfolgentabelle**
</dt> <dd>

Eine numerische Konstante, die in einer [**\# define-Anweisung**](-define.md) definiert ist, muss unmittelbar auf das **BEGIN-Schlüsselwort** in einer [**STRINGTABLE-Anweisung**](stringtable-resource.md) folgen.

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Erwartete numerische Punktgröße**
</dt> <dd>

Der *Pointsize-Parameter* der [**FONT-Anweisung**](font-statement.md) in der [**DIALOG-Anweisung**](dialog-resource.md) muss ein ganzzahliger Punktgrößenwert sein.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Erwartete numerische Dialogkonstante**
</dt> <dd>

Eine [**DIALOG-Anweisung**](dialog-resource.md) erfordert ganzzahlige Werte für die Parameter *x,* *y,* *width* und *height.* Stellen Sie sicher, dass diese Werte, die nach dem **DIALOG-Schlüsselwort** enthalten sind, nicht negativ sind.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Erwartete Zeichenfolge in STRINGTABLE**
</dt> <dd>

Eine Zeichenfolge wird nach jedem numerischen *stringid-Parameter* in einer [**STRINGTABLE-Anweisung**](stringtable-resource.md) erwartet.

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Erwarteter String- oder Constant Accelerator-Befehl**
</dt> <dd>

Der Microsoft Windows Resource Compiler (RC) konnte nicht ermitteln, welcher Schlüssel für die Zugriffstaste eingerichtet wurde. Der *Ereignisparameter* in der [**ACCELERATORS-Anweisung**](accelerators-resource.md) ist möglicherweise ungültig.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Value-, BLOCK- oder END-Schlüsselwort erwartet.**
</dt> <dd>

Die [**VERSIONINFO-Struktur**](versioninfo-resource.md) erfordert ein **VALUE-,** **BLOCK-** oder **END-Schlüsselwort.**

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Erwartete Zahl für ID**
</dt> <dd>

Für den *ID-Parameter* einer [**CONTROL-Anweisung**](control-control.md) in der [**DIALOG-Anweisung**](dialog-resource.md) wird eine Zahl erwartet. Stellen Sie sicher, dass Sie über eine Zahl oder eine [**\# define-Anweisung**](-define.md) für den Steuerelementbezeichner verfügen.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Erwarten einer Zeichenfolge in Anführungszeichen für den Schlüssel**
</dt> <dd>

Die Schlüsselzeichenfolge nach dem **BLOCK-** oder **VALUE-Schlüsselwort** sollte in doppelte Anführungszeichen eingeschlossen werden.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Erwarten einer Zeichenfolge in Anführungszeichen in der Dialogklasse**
</dt> <dd>

Der *Klassenparameter* der [**CLASS-Anweisung**](class-statement.md) in der [**DIALOG-Anweisung**](dialog-resource.md) muss eine ganze Zahl oder eine Zeichenfolge sein, die in doppelte Anführungszeichen (") eingeschlossen ist.

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Erwarten einer Zeichenfolge in Anführungszeichen im Dialogtitel**
</dt> <dd>

Der *captiontext-Parameter* der [**CAPTION-Anweisung**](caption-statement.md) in der [**DIALOG-Anweisung**](dialog-resource.md) muss eine Zeichenfolge sein, die in doppelte Anführungszeichen (") eingeschlossen ist.

</dd> </dl>

 

 




