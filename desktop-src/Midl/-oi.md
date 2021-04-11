---
title: /Oi-Schalter
description: Die Schalter/Oi und/OIC leiten den Mittel l-Compiler an die Verwendung einer vollständig interpretierten Marshallingmethode. Der/Oicf-Schalter bietet weitere Leistungsverbesserungen.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208868"
---
# <a name="oi-switch"></a>/Oi-Schalter

Die Schalter **/Oi** und **/OIC** leiten den Mittel l-Compiler an die Verwendung einer vollständig interpretierten Marshallingmethode. Der **/Oicf** -Schalter bietet weitere Leistungsverbesserungen.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Zählen* 
</dt> <dd>

Gibt die vollständig interpretierte Methode zum Marshalling von Stub-Code an, der zwischen Client und Server übermittelt wird.

> [!Note]  
> Dieser Schalter ist veraltet. Es wird empfohlen, dass der Schalter **/Oicf** verwendet wird.

 

</dd> <dt>

*OIC* 
</dt> <dd>

Gibt die ohne Code-Proxy Methode für das Marshalling an, das alle Features von **/Oi** bereitstellt und außerdem die Größe des Client-Stub-Codes für Objekt Schnittstellen weiter reduziert.

> [!Note]  
> Dieser Schalter ist veraltet. Es wird empfohlen, dass der Schalter **/Oicf** verwendet wird.

 

</dd> <dt>

*OIF oder Oicf* 
</dt> <dd>

Gibt die coschess-Proxy Methode für das Marshalling an, das alle von **/Oi** und **/OIC** bereitgestellten Features umfasst, aber einen neuen Interpreter (schnelle Format Zeichenfolgen) verwendet, der eine bessere Leistung als **/Oi** oder **/OIC** bietet. Dieser Switch umfasst aktuelle RPC-Erweiterungen und wird für moderne RPC-Szenarien empfohlen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie die Einschränkungen in Bezug auf die unterstützenden Plattformen.

Der Compiler für die Mittel l 3,0 bietet zwei Methoden zum Mars Hallen von Code: vollständig interpretiert ( **/Oi**, **/OIC** und **/Oicf**) und gemischter Modus ( [**/OS**](-os.md)). Beginnend mit der basl-Version 6.0.359 generiert der Mittelwert Compiler standardmäßig **/Oicf**- [**/robust**](-robust.md) -stubwerte. Einige sprach Features werden in einigen Modi nicht unterstützt. In diesem Fall wechselt der Compiler automatisch in den entsprechenden Modus und gibt eine Warnung aus.

Wenn die Leistung von Bedeutung ist, kann die Methode mit gemischtem Modus ( [**/OS**](-os.md)) die beste Methode sein. In diesem Modus wählt der Compiler, dass einige Parameter in den generierten stubflächen Inline gemarshallt werden. Dies führt zwar zu einer größeren stubgröße, bietet jedoch eine höhere Leistung.

Die vollständig interpretierte Methode Marshalls Daten vollständig offline. Dadurch wird die Größe des stubcodes beträchtlich reduziert, dies führt jedoch zu einer geringeren Leistung. Außerdem gibt es bei der voll interpretierten Methode eine Beschränkung von 16 Parametern für jede Prozedur. Jede Prozedur, die mehr als 16 Parameter enthält, wird automatisch im [**/OS**](-os.md) -Modus verarbeitet. Unter den interpretierten Modi bietet **/Oicf** die beste Leistung, und **/Oi** bietet die beste Abwärtskompatibilität.

Möglicherweise möchten Sie die **/OIF** -Option verwenden, wenn Ihre Anwendung in der Mitte 3,0 eingeführte Mittel l-Funktionen verwendet, wie z \[ . b. das [**Wire \_ Marshal**](wire-marshal.md) \] -Attribut und das \[ [**User \_ Marshal**](user-marshal.md) - \] Attribut. Wenn Ihre Anwendung [Pipes](/windows/desktop/Rpc/pipes) verwendet, müssen Sie die **/OIF** -Option verwenden. Wenn Sie einen anderen Modus angeben, wechselt der Mittell-Compiler zu **/OIF**.

Zum Optimieren der Art und Weise, in der der Stubcode gemarshallt wird, bietet Microsoft RPC ein ACF- \[ [**Optimierungs**](optimize.md) \] Attribut. Dieses Attribut wird als Schnittstellen Attribut oder Vorgangs Attribut verwendet, um den marshallingmodus für einzelne Schnittstellen oder für einzelne Vorgänge auszuwählen.

### <a name="calling-conventions"></a>Aufrufkonventionen

Vom Mittel l-Compiler in der interpretierten Methode mithilfe der **/Oi**-, **/OIC**-oder **/OIF** -Switches generierte Stub müssen während der C-Kompilierung entweder als stdcall-oder als cdecl-Prozedur kompiliert werden. Eine Pascal-oder Fastcall-Aufruf Konvention funktioniert nicht. Außerdem muss der Stub des Servers als stdcallkompiliert werden.

## <a name="examples"></a>Beispiele

**Mittel l/Oi Dateiname. idl**

**Mittel l/OIC Dateiname. idl**

**Mittel l/OIF Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**/No \_ robust**](-no-robust.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OS**](-os.md)
</dt> <dt>

[**optimiert**](optimize.md)
</dt> <dt>

[**/No \_ Format \_ Opt**](-no-format-opt.md)
</dt> </dl>

 

 