---
title: /out-Schalter
description: Der/out-Schalter gibt das Standardverzeichnis an, in dem der Mittell-Compiler Ausgabedateien schreibt.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338032"
---
# <a name="out-switch"></a>/out-Schalter

Der **/out** -Schalter gibt das Standardverzeichnis an, in dem der Mittell-Compiler Ausgabedateien schreibt.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Path-Spezifikation* 
</dt> <dd>

Gibt den Pfad zu dem Verzeichnis an, in dem die Stub-, Header-und switchdateien generiert werden. Es kann eine Laufwerk Spezifikation, ein absoluter Verzeichnispfad oder beides angegeben werden. Pfade können mit doppelten Anführungszeichen (") explizit in Anführungszeichen eingeschlossen werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ausgabeverzeichnis kann mit einem Laufwerk Buchstaben, einem absoluten Pfadnamen oder beidem angegeben werden. Die **/out** -Option kann mit allen Schaltern verwendet werden, die die Angabe einzelner Ausgabedateien ermöglichen.

Wenn der Schalter **/out** nicht angegeben wird, werden die Dateien in das aktuelle Verzeichnis geschrieben.

Das vom **/out** -Schalter angegebene Standardverzeichnis kann durch einen expliziten Pfadnamen überschrieben werden, der als Teil des [**/cstub**](-cstub.md)-, [**/Header**](-header.md)-, [**/Proxy**](-proxy.md)-oder [**/sstub**](-sstub.md) -Schalters angegeben wird.

## <a name="examples"></a>Beispiele

**Mittel l/Out c: \\ "MyDir" \\ meinsubdir \\ SubDir2 tiefere Dateinamen. idl**

**Mittel l/Out c: Dateiname. idl**

**Mittel l/out \\ "MyDir" \\ mysubdir \\ ein anderer Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/Proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




