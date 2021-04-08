---
title: E (Menüs und andere Ressourcen)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102750"
---
# <a name="e-menus-and-other-resources"></a>E (Menüs und andere Ressourcen)

[a](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Leere Menüs sind nicht zulässig.**
</dt> <dd>

Ein **End** -Schlüsselwort wird angezeigt, bevor beliebige Menü Elemente in der [**Menü**](menu-resource.md) Anweisung definiert werden. Leere Menüs sind vom Microsoft Windows 32 Resource Compiler (RC) nicht zulässig. Stellen Sie sicher, dass in der **Menü** Anweisung keine öffnenden Anführungszeichen vorhanden sind.

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Ende erwartet in Dialog Feld**
</dt> <dd>

Das **End** -Schlüsselwort muss am Ende einer [**Dialog**](dialog-resource.md) Feld Anweisung angezeigt werden. Stellen Sie sicher, dass die vorangehende Anweisung keine öffnenden Anführungszeichen enthält.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**Ende im Menü erwartet**
</dt> <dd>

Das **End** -Schlüsselwort muss am Ende einer [**Menü**](menu-resource.md) Anweisung angezeigt werden. Stellen Sie sicher, dass keine übereinstimmenden **Begin** -und **End** -Anweisungen vorhanden sind.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Fehler bei "kreatingresource-Name".**
</dt> <dd>

Die angegebene binäre Ressource konnte von Microsoft Windows 32 Resource Compiler (RC) nicht erstellt werden. RES-Datei). Stellen Sie sicher, dass er nicht auf einem schreibgeschützten Laufwerk erstellt wird. Verwenden Sie die Option **/v** , um herauszufinden, ob die Datei erstellt wird.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Komma in Zugriffstasten Tabelle erwartet**
</dt> <dd>

Der Microsoft Windows 32-Ressourcen Compiler (RC) erfordert ein Komma zwischen den Parametern " *Event* " und " *idValue* " in der [**Accelerators**](accelerators-resource.md) -Anweisung.

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Name der Steuerelement Klasse erwartet**
</dt> <dd>

Der *Class* -Parameter einer [**Control**](control-control.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss einer der folgenden Steuerelement Typen sein: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** oder User-Defined. Stellen Sie sicher, dass die-Klasse korrekt geschrieben ist.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Der Name der Schriftart wurde erwartet.**
</dt> <dd>

Der *Schriftart-Parameter* der **Font** -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist. Dieser Parameter gibt den Namen einer Schriftart an.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Erwarteter ID-Wert für MenuItem.**
</dt> <dd>

Die [**Menu**](menu-resource.md) -Anweisung muss eine [**MenuItem**](menuitem-statement.md) -Anweisung enthalten, die entweder eine Ganzzahl oder eine symbolische Konstante im *MENUID* -Parameter aufweist.

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Erwartete Menü Zeichenfolge**
</dt> <dd>

Jede [**MenuItem**](menuitem-statement.md) -und [**Popup**](popup-resource.md) -Anweisung muss einen *Text* Parameter enthalten. Dieser Parameter ist eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die den Namen des Menü Elements oder Popup Menüs angibt. Eine **MENUITEM SEPARATOR** -Anweisung erfordert keine Zeichenfolge in Anführungszeichen.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Numerischer Befehls Wert erwartet.**
</dt> <dd>

Der Microsoft Windows-Ressourcen Compiler (RC) hat einen numerischen *idValue* -Parameter in der [**Accelerators**](accelerators-resource.md) -Anweisung erwartet. Stellen Sie sicher, dass Sie eine [**\# define**](-define.md) -Anweisung verwendet haben, um den Wert anzugeben, und dass die verwendete Konstante korrekt geschrieben ist.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Numerische Konstante in Zeichen folgen Tabelle erwartet**
</dt> <dd>

Eine in einer [**\# define**](-define.md) -Anweisung definierte numerische Konstante muss direkt auf das **Begin** -Schlüsselwort in einer [**STRINGTABLE**](stringtable-resource.md) -Anweisung folgen.

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Erwartete numerische Punktgröße**
</dt> <dd>

Der *pointsize* -Parameter der [**Font**](font-statement.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss ein ganzzahliger Wert für die Punktgröße sein.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Numerische Dialog Konstante erwartet**
</dt> <dd>

Eine [**Dialog**](dialog-resource.md) Feld Anweisung erfordert *ganzzahlige* Werte für die Parameter *x*, y, *Width* und *height* . Stellen Sie sicher, dass diese Werte, die nach dem **Dialog** Feld Schlüsselwort enthalten sind, nicht negativ sind.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Erwartete Zeichenfolge in STRINGTABLE**
</dt> <dd>

Nach jedem numerischen *stringID* -Parameter in einer [**STRINGTABLE**](stringtable-resource.md) -Anweisung wird eine Zeichenfolge erwartet.

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Erwarteter String-oder Constant Accelerator-Befehl**
</dt> <dd>

Der Microsoft Windows-Ressourcen Compiler (RC) konnte nicht ermitteln, welcher Schlüssel für die Zugriffstaste eingerichtet wurde. Der *Ereignis* Parameter in der [**Accelerators**](accelerators-resource.md) -Anweisung ist möglicherweise ungültig.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Erwartetes Wert-, Block-oder End-Schlüsselwort.**
</dt> <dd>

Die [**VERSIONINFO**](versioninfo-resource.md) -Struktur erfordert ein **value**-, **Block**-oder **End** -Schlüsselwort.

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Anzahl für ID wird erwartet.**
</dt> <dd>

Eine Zahl wird für den *ID* -Parameter einer [**Steuer**](control-control.md) Element Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung erwartet. Stellen Sie sicher, dass Sie über eine Zahl oder eine [**\# define**](-define.md) -Anweisung für den Steuerelement Bezeichner verfügen.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Zeichenfolge in Anführungszeichen für Schlüssel erwartet**
</dt> <dd>

Die Schlüssel Zeichenfolge nach dem **Block** -oder **value** -Schlüsselwort sollte in doppelte Anführungszeichen eingeschlossen werden.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Zeichenfolge in Anführungszeichen in Dialog Klasse erwartet**
</dt> <dd>

Der *Class* -Parameter der [**Class**](class-statement.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss eine ganze Zahl oder eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Zeichenfolge in Anführungszeichen in Dialogfeld Titel erwartet**
</dt> <dd>

Der *CaptionText* -Parameter der [**Caption**](caption-statement.md) -Anweisung in der [**Dialog**](dialog-resource.md) -Anweisung muss eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.

</dd> </dl>

 

 




