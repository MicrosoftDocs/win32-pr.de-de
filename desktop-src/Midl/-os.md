---
title: /OS-Schalter
description: Der Schalter/OS gibt die Methode im gemischten Modus an, um Stubcode zu Mars Hallen, der zwischen Client und Server übermittelt wird.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /OS-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340460"
---
# <a name="os-switch"></a>/OS-Schalter

Der Schalter **/OS** gibt die Methode im gemischten Modus an, um Stubcode zu Mars Hallen, der zwischen Client und Server übermittelt wird.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Es gibt wichtige Punkte, die Sie berücksichtigen sollten, bevor Sie sich für die Methode zum Marshalling von Code entscheiden. Diese Probleme betreffen die Größe und Leistung. Der mittlerer l-Compiler stellt zwei Methoden zum Mars Hallen von Code bereit: gemischter Modus (**/OS**) und vollständig interpretiert ([**/Oi**](-oi.md)). Die vollständig interpretierte Methode Marshalls Daten vollständig offline. Dadurch wird die Größe des stubcodes beträchtlich reduziert, dies führt jedoch auch zu einer geringeren Leistung.

Verwenden Sie den mittleren l-Standardmodus **/Oicf** /robust für alle anderen Zwecke als die Abwärtskompatibilität. Dieser Modus ist der sichere Standardmodus des Mittel l-Compilers. jeder andere Modus sollte nur nach sorgfältiger Überlegung der Sicherheits Implikation verwendet werden, um zu erkennen, dass zukünftige Erweiterungen nur für den Standardmodus implementiert werden. Im gemischten Modus Marshalls der Compiler einige Parameter inline in den generierten stubmodus. Dies führt zwar zu einer größeren stubgröße, bietet jedoch möglicherweise eine höhere Leistung.

Die mittlere Unterstützung für mehrdimensionale Arrays und Zeiger mit mehrdimensionalen Größen ist nur im [**/Oicf**](-oi.md) -Modus enthalten. In den Modi **/OS** und **/Oi** unterstützt der Compiler einfache Fälle, z. b. Arrays mit fester Größe. Die Verwendung von mehrdimensionalen Arrays im **/OS** -oder **/Oi** -Modus kann zu Parametern führen, die nicht ordnungsgemäß gemarshallt werden Microsoft empfiehlt die Verwendung des Befehls Zeilenschalters **/Oicf** , wenn Ihre Schnittstelle Parameter definiert, die mehrdimensionale Arrays oder Zeiger mit mehrdimensionalen Größen sind.

Zum weiteren definieren der gradgradgradgradmenge in der Art und Weise, in der Daten gemarshallt werden, stellt diese RPC- \[ [](optimize.md) Version ein \] Dieses Attribut wird als ACF-Schnittstellen Attribut oder Vorgangs Attribut verwendet, um den marshallingmodus auszuwählen.

## <a name="examples"></a>Beispiele

**Mittel l/OS Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**optimiert**](optimize.md)
</dt> <dt>

[**/No \_ Format \_ Opt**](-no-format-opt.md)
</dt> </dl>

 

 




