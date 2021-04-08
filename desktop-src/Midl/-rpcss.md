---
title: /RPCSS-Schalter
description: Wenn der/RPCSS-Schalter angegeben wird, verhält er sich so, als ob das Enable- \_ Attribut "zuordnen" für alle Vorgänge der Schnittstelle angegeben wurde. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /RPCSS-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037838"
---
# <a name="rpcss-switch"></a>/RPCSS-Schalter

Wenn der **/RPCSS** -Schalter angegeben wird, verhält er sich so, als ob das Enable-Attribut " [**\_ zuordnen**](enable-allocate.md) " für alle Vorgänge der Schnittstelle angegeben wurde. Die Verwendung dieses Attributs wird nicht empfohlen.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Im Standardmodus ist das RPCSS-Paket nur aktiviert, wenn entweder die Prozedur oder die Schnittstelle über das Attribut " [**\_ zuordnen**](enable-allocate.md) " verfügen oder der Schalter " **/RPCSS** " in der Befehlszeile angegeben ist. Im **/OSF** -Modus aktiviert der serverseitige Stub das RPCSS-Zuordnungs Paket.

## <a name="examples"></a>Beispiele

**Mittel l/RPCSS Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_zuordnen aktivieren**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




