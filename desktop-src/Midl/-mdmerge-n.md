---
title: Schalter "/n"
description: Der Schalter /n gibt die Kompositionstiefe zum Erstellen von Metadatendateien an.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n switch MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b54473b282976d2ab871db0f1699c1154070a3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886047"
---
# <a name="n-switch"></a>Schalter "/n"

Der **Schalter /n** gibt die Kompositionstiefe zum Erstellen von Metadatendateien an.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*\_Namespacetiefe* 
</dt> <dd>

Gibt die Namespacetiefe an, die in einer einzelnen Metadatendatei erstellt werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die möglichen Wertformate, die Sie mit dem **Schalter /n angeben** können.



| Wertformat                   | Beschreibung                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Erstellen Sie alle Typen in der Namespacetiefe, die im Schalter angegeben ist.               |
| -1                             | Erstellen Sie alle Typen in einer IDL-Datei pro Namespace.                              |
| &lt;&gt;namespace:Int32 > 0 | Erstellen Sie alle Typen mit übereinstimmenden Namespaces in der im Schalter angegebenen Tiefe. |
| &lt;namespace &gt; :-1           | Erstellen Sie alle Typen mit übereinstimmenden Namespaces in einer Datei pro Namespace.          |



 

Die folgende Tabelle zeigt die Ergebnisse aus verschiedenen Kombinationen des **Schalters /n,** die für diese Namespaces funktionieren.

-   Windows. Foundation.Collections.IIterable
-   Windows. BENUTZEROBERFLÄCHE. DirectUI.Controls.Button
-   Windows. BENUTZEROBERFLÄCHE. DirectUI.Controls.ListView
-   Windows. BENUTZEROBERFLÄCHE. Immersive.Application.PlayTo.Target
-   Windows. Web.Syndication.RSS



| Switches                         | Ergebnis                                                                                                                                                                                                                                                       | Erklärung                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | Der letzte /n-Schalter überschreibt alle vorherigen –n-Schalter.                                                                                                                                                                                                                                                                           |
| **/n:-1/n:Windows. UI:2**         | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. UI.winmd</dt> <dt>Windows. Web.Syndication.winmd</dt> </dl> | <dl> <dt>**Windows. Die** Grundlage wird immer bei –n:2 zusammengestellt.</dt> <dt>**Windows. Benutzeroberflächentypen** werden gruppiert.</dt> <dt>**Windows. Web.Syndication** besteht aus n:-1.</dt> </dl>       |
| **/n:1/n:Windows. BENUTZEROBERFLÄCHE. DirectUI:3** | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. BENUTZEROBERFLÄCHE. DirectUI.winmd</dt> <dt>Windows.winmd</dt> </dl>       | <dl> <dt>**Windows. Die** Grundlage wird immer bei –n:2 zusammengestellt.</dt> <dt>**Windows. BENUTZEROBERFLÄCHE. DirectUI** setzt sich auf Ebene 3 zusammen.</dt> <dt>Alle anderen Typen werden auf Ebene 1 zusammengesetzt.</dt> </dl> |



 

Hier sind die Regeln für die Behandlung mehrerer Instanzen des **Schalters /n.**

-   Die spezifischste Instanz ist nicht der Fall. Wenn Sie beispielsweise **–n:A.B.C:4-n:A.B:5** angeben, löst MDMERGE A.B.C.D auf Ebene 4 auf, da A.B.C spezifischer als A.B. ist. A.B.E.F wird in Tiefe 5 auflösen, da es A.B, aber nicht A.B.C. entspricht.
-   Die letzte Instanz ist nicht mehr zu sehen. Wenn Sie beispielsweise **–n:5-n:2** angeben, bestehen die Typen auf Ebene 2.
-   Beide Regeln gelten. Wenn Sie –n:A.B.C:4 –n:A.B.C:1 angeben, besteht der Namespace A.B.C auf Ebene 1.

## <a name="examples"></a>Beispiele

**mdmerge.exe -metadata \_ dir $(SDK \_ METADATA \_ PATH) -i $(INTERNAL \_ SDK METADATA \_ \_ PATH) -o $(OBJ \_ PATH) $O \\ \\ SystemMetadata -v -n:-1 -n:Windows. Foundation:2**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------|
| Client<br/> | Windows 8<br/>           |
| Server<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





