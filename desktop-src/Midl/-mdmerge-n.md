---
title: /n switch
description: Der Schalter /n gibt die Kompositionstiefe für das Zusammenstellen von Metadatendateien an.
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
ms.openlocfilehash: d3e9575995d80a4c61b5e91be7c5cfc1c802abed892af8cfa653f62c66e602b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430970"
---
# <a name="n-switch"></a>/n switch

Der Schalter **/n** gibt die Kompositionstiefe für das Zusammenstellen von Metadatendateien an.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_Namespacetiefe* 
</dt> <dd>

Gibt die Namespacetiefe an, die in einer einzelnen Metadatendatei erstellt werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Hier sind die möglichen Wertformate, die Sie mit dem Schalter **/n** angeben können.



| Wertformat                   | Beschreibung                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Erstellen Sie alle Typen in der im Schalter angegebenen Namespacetiefe.               |
| -1                             | Erstellen Sie alle Typen in einer IDL-Datei pro Namespace.                              |
| <namespace>:Int32 > 0 | Erstellen Sie alle Typen mit übereinstimmenden Namespaces in der im Schalter angegebenen Tiefe. |
| <namespace>:-1           | Erstellen Sie alle Typen mit übereinstimmenden Namespaces in einer Datei pro Namespace.          |



 

Die folgende Tabelle zeigt die Ergebnisse verschiedener Kombinationen des **Schalters /n,** die an diesen Namespaces arbeiten.

-   Windows. Foundation.Collections.IIterable
-   Windows. Benutzeroberfläche. DirectUI.Controls.Button
-   Windows. Benutzeroberfläche. DirectUI.Controls.ListView
-   Windows. Benutzeroberfläche. Immersive.Application.PlayTo.Target
-   Windows. Web.Syndication.RSS



| Optionen                         | Ergebnis                                                                                                                                                                                                                                                       | Erklärung                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | Der letzte /n-Schalter überschreibt alle vorherigen –n Schalter.                                                                                                                                                                                                                                                                           |
| **/n:-1/n:Windows. Benutzeroberfläche:2**         | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. UI.winmd</dt> <dt>Windows. Web.Syndication.winmd</dt> </dl> | <dl> <dt>**Windows. Die Basis** wird immer bei –n:2 zusammengesetzt.</dt> <dt>**Windows. Benutzeroberflächentypen** werden gruppiert.</dt> <dt>**Windows. Web.Syndication** besteht aus n:-1.</dt> </dl>       |
| **/n:1/n:Windows. Benutzeroberfläche. DirectUI:3** | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. Benutzeroberfläche. DirectUI.winmd</dt> <dt>Windows.winmd</dt> </dl>       | <dl> <dt>**Windows. Die Basis** wird immer bei –n:2 zusammengesetzt.</dt> <dt>**Windows. Benutzeroberfläche. DirectUI** besteht aus Ebene 3.</dt> <dt>Alle anderen Typen werden auf Ebene 1 zusammengesetzt.</dt> </dl> |



 

Hier sind die Regeln für die Behandlung mehrerer Instanzen des Schalters **/n.**

-   Die spezifischste Instanz tritt auf. Wenn Sie beispielsweise **–n:A.B.C:4-n:A.B:5** angeben, löst MDMERGE A.B.C.D auf Ebene 4 auf, da A.B.C spezifischer als A.B. B ist. A.B.E.F wird in Tiefe 5 aufgelöst, da es A.B, aber nicht A.B.C entspricht.
-   Die letzte Instanz ist nicht mehr vorhanden. Wenn Sie beispielsweise **–n:5–n:2** angeben, werden die Typen auf Ebene 2 zusammengesetzt.
-   Beide Regeln gelten. Wenn Sie –n:A.B.C:4 –n:A.B.C:1 angeben, wird namespace A.B.C auf Ebene 1 zusammengesetzt.

## <a name="examples"></a>Beispiele

**mdmerge.exe -metadata \_ dir $(SDK \_ METADATA \_ PATH) -i $(INTERNAL \_ SDK METADATA \_ \_ PATH) -o $(OBJ \_ PATH) $O \\ \\ SystemMetadata -v -n:-1 -n:Windows. Foundation:2**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------|
| Client<br/> | Windows 8<br/>           |
| Server<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





