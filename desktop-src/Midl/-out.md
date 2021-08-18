---
title: /out-Schalter
description: Der Schalter /out gibt das Standardverzeichnis an, in das der MIDL-Compiler Ausgabedateien schreibt.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out switch MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b29c97438c0db1a60d94a8ae88ed99f73c33ea16a820d1aec5ca7a6be737e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014098"
---
# <a name="out-switch"></a>/out-Schalter

Der **Schalter /out** gibt das Standardverzeichnis an, in das der MIDL-Compiler Ausgabedateien schreibt.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*path-specification* 
</dt> <dd>

Gibt den Pfad zu dem Verzeichnis an, in dem die Stub-, Header- und Switchdateien generiert werden. Eine Laufwerkspezifikation, ein absoluter Verzeichnispfad oder beides kann angegeben werden. Pfade können explizit mit doppelten Anführungszeichen (") in Anführungszeichen angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Ausgabeverzeichnis kann mit einem Laufwerkbuchstaben, einem absoluten Pfadnamen oder beidem angegeben werden. Die **Option /out** kann mit jedem der Schalter verwendet werden, die eine individuelle Ausgabedateispezifikation ermöglichen.

Wenn der **Schalter /out** nicht angegeben ist, werden Dateien in das aktuelle Verzeichnis geschrieben.

Das vom Schalter **/out** angegebene Standardverzeichnis kann durch einen expliziten Pfadnamen überschrieben werden, der als Teil des Schalters [**/cstub,**](-cstub.md) [**/header,**](-header.md) [**/proxy**](-proxy.md)oder [**/sstub angegeben**](-sstub.md) ist.

## <a name="examples"></a>Beispiele

**midl /out c: \\ mydir \\ mysubdir \\ subdir2 deeper filename.idl**

**midl /out c: filename.idl**

**midl /out \\ mydir \\ mysubdir \\ another filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




