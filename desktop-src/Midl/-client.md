---
title: /Client-Schalter
description: Der/Client-Schalter weist den Mittelwert Compiler an, Client seitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /Client-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312960"
---
# <a name="client-switch"></a>/Client-Schalter

Der **/Client** -Schalter weist den Mittelwert Compiler an, Client seitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>Stub * * * *


</dt> <dd>

Generiert die Client seitigen Dateien.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>keine * * * *


</dt> <dd>

Generiert keine Client seitigen Dateien.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der **/Client** -Schalter nicht angegeben wird, generiert der kompilierungscompiler die clientstubdatei. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Der **/Client** -Schalter hat Vorrang vor dem [**/cstub**](-cstub.md) -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/Client keine Datei Name. idl**

**Mittel l/Client Stub-Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Server**](-server.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




