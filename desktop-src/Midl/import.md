---
title: import-Attribut
description: Die Import-Direktive gibt eine andere IDL-, ODL-oder Header Datei an, die Definitionen enthält, auf die Sie aus der IDL-Hauptdatei verweisen möchten
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- Import Attribut-Mittel l
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314768"
---
# <a name="import-attribute"></a>import-Attribut

Die **Import** -Direktive gibt eine andere IDL-, ODL-oder Header Datei an, die Definitionen enthält, auf die Sie aus der IDL-Hauptdatei verweisen möchten

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*filename* 
</dt> <dd>

Gibt den Namen der zu importierenden Header-, IDL-oder ODL-Datei an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der **Import** -Direktive werden alle IDL-Anweisungen in der importierten Datei (z. b. Typedefs, Konstante Deklarationen und Schnittstellendefinitionen) für den Import verfügbar. IDL-Datei.

Die importierte Datei wird separat verarbeitet (d. h., dass der CPP-Präprozessor unabhängig aufgerufen wird) aus der importierenden IDL-Datei. Auf diese Weise führen Präprozessordirektiven, wie z. b. \# define, nicht aus einer importierten Header-oder IDL-Datei in die importierende IDL-Datei.

Wie das Präprozessormakro in der C-Sprache weist die **Import** -Direktive den Compiler an, Datentypen einzuschließen, die in den importierten IDL-Dateien definiert wurden. **\#** Anders als bei der **\# include** -Direktive ignoriert die **Import** -Direktive Prozedur Prototypen, da für Elemente in der importierten Datei keine Stubdaten generiert werden.

Spezifische Informationen zum Verwenden von **Import** zum Einschließen von Header Dateien in eine IDL-Datei finden Sie unter [Importieren von System Header Dateien](importing-system-header-files.md).

Der C-sprach Header (. H) die für die Schnittstelle generierte Datei enthält nicht direkt die importierten Typen, sondern generiert stattdessen eine **\# include** -Direktive für die Header Datei, die der importierten Schnittstelle entspricht. Dies ist beispielsweise der Fall, wenn Sie Base importieren. IDL in Ihre abgeleitete. IDL, die generierte Header Datei, die abgeleitet wurde. H enthält die Direktive **\# include** Base. h.

Es gelten die folgenden Regeln:

-   Das **Import** -Schlüsselwort ist optional und kann in der IDL-Datei null oder mehrmals vorkommen.
-   Jedem **Import** Schlüsselwort können mehr als ein Dateiname zugeordnet werden.
-   Trennen Sie mehrere Dateinamen durch Kommas.
-   Sie müssen den Dateinamen in Anführungszeichen einschließen und die Import Anweisung mit einem Semikolon (;)) beenden.
-   Sie können eine Schnittstelle, die über keine Attribute verfügt, in eine andere IDL-Datei importieren. Die Schnittstelle darf jedoch nur Datentypen enthalten. Er darf keine Prozeduren enthalten. Wenn auch eine Prozedur in der importierten Schnittstelle enthalten ist, müssen Sie ein [**Lokales**](local.md) Attribut oder ein [**UUID**](uuid.md) -Attribut angeben.
-   Die **Import** Funktion ist idemtypfähig. das heißt, dass das Importieren einer Schnittstelle mehr als einmal keine weiteren Auswirkungen hat.

> [!Note]  
> Das Verhalten der **Import** Direktive ist unabhängig von den [**/MS \_ ext**](-ms-ext.md) (Standard), [**/OSF**](-osf.md)und [**/App \_**](-app-config.md). Der Compilermodus (**/OSF** oder **/MS \_ ext**) kann sich jedoch auf die Zeiger Attribut Ergänzung für importierte Typen auswirken. Weitere Informationen finden Sie unter [Pointer-Attribute Type-Vererbung](/windows/desktop/Rpc/pointer-attribute-type-inheritance).

 

## <a name="examples"></a>Beispiele

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/APP- \_ Konfiguration**](-app-config.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**darunter**](include.md)
</dt> <dt>

[Importieren von System-Headerdateien](importing-system-header-files.md)
</dt> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 