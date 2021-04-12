---
title: /oldtlb-Schalter
description: Der/oldtlb-Schalter weist den Mittel l-Compiler an, eine Typbibliothek im alten Format zu generieren.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390202"
---
# <a name="oldtlb-switch"></a>/oldtlb-Schalter

Der **/oldtlb** -Schalter weist den Mittel l-Compiler an, eine Typbibliothek im alten Format zu generieren.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Der **/oldtlb** -Schalter überschreibt den Standardwert und leitet den Mittelwert des compl-Compilers so um, dass Typbibliotheken im alten Format selbst bei aktuellen Versionen von Windows generiert werden [, indem "" anstelle von](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) " [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2)" die Verwendung von "

## <a name="examples"></a>Beispiele

**Mittel l/oldtlb Dateiname. idl**

**Mittel l/oldtlb myoldodl. ODL**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 