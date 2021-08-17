---
title: /Oi-Schalter
description: Die Schalter /Oi und /Oic leiten den MIDL-Compiler an, eine vollständig interpretierte Marshallingmethode zu verwenden. Der Schalter /Oicf bietet zusätzliche Leistungsverbesserungen.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi switch MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38b6faee202e15b7c551297678ce301cbfdcb853b48ecd15c75dda7bb281e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385284"
---
# <a name="oi-switch"></a>/Oi-Schalter

Die Schalter **/Oi** und **/Oic** leiten den MIDL-Compiler an, eine vollständig interpretierte Marshallingmethode zu verwenden. Der Schalter **/Oicf** bietet zusätzliche Leistungsverbesserungen.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Oi* 
</dt> <dd>

Gibt die vollständig interpretierte Methode zum Marshallen von Stubcode an, der zwischen Client und Server übergeben wird.

> [!Note]  
> Dieser Schalter ist veraltet. Es wird empfohlen, den Schalter **/Oicf** an seiner Stelle zu verwenden.

 

</dd> <dt>

*Oic* 
</dt> <dd>

Gibt die codelose Proxymethode für das Marshalling an, die alle Funktionen von **/Oi** bereitstellt und außerdem die Größe des Clientstubcodes für Objektschnittstellen weiter reduziert.

> [!Note]  
> Dieser Schalter ist veraltet. Es wird empfohlen, den Schalter **/Oicf** an seiner Stelle zu verwenden.

 

</dd> <dt>

*Oif oder Oicf* 
</dt> <dd>

Gibt die codelose Proxymethode für das Marshalling an, die alle von **/Oi** und **/Oic** bereitgestellten Funktionen umfasst, aber einen neuen Interpreter (schnelle Formatzeichenfolgen) verwendet, der eine bessere Leistung als **/Oi** oder **/Oic** bietet. Dieser Schalter enthält aktuelle RPC-Erweiterungen und wird für moderne RPC-Szenarien empfohlen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie die Einschränkungen im Zusammenhang mit unterstützenden Plattformen.

Der MIDL 3.0-Compiler stellt zwei Methoden zum Marshallen von Code bereit: vollständig interpretiert ( **/Oi**, **/Oic** und **/Oicf**) und gemischter Modus ( [**/Os**](-os.md)). Ab MIDL-Version 6.0.359 generiert der MIDL-Compiler standardmäßig **/Oicf** Â [**/robust**](-robust.md) stubs. Einige Sprachfeatures werden in einigen Modi nicht unterstützt. In diesem Fall wechselt der Compiler automatisch in den entsprechenden Modus und gibt eine Warnung aus.

Wenn die Leistung ein Problem ist, kann die Methode im gemischten Modus ( [**/Os**](-os.md)) der beste Ansatz sein. In diesem Modus wählt der Compiler aus, einige Parameter inline in den generierten Stubs zu marshallen. Dies führt zwar zu einer größeren Stubgröße, bietet aber eine höhere Leistung.

Die vollständig interpretierte Methode marshallt Daten vollständig offline. Dadurch wird die Größe des Stubcodes erheblich reduziert, die Leistung wird jedoch verringert. Außerdem gilt bei der vollständig interpretierten Methode ein Grenzwert von 16 Parametern für jede Prozedur. Jede Prozedur, die mehr als 16 Parameter enthält, wird automatisch im [**Modus "/Os"**](-os.md) verarbeitet. Unter den interpretierten Modi bietet **/Oicf** die beste Leistung und **/Oi** die beste Abwärtskompatibilität.

Sie können die Option **/Oif** verwenden, wenn Ihre Anwendung MIDL-Features verwendet, die mit MIDL 3.0 eingeführt wurden, z. B. das \[ [**Wire \_ Marshal-**](wire-marshal.md) \] und das \[ [**\_ Benutzer-Marshallal-Attribut.**](user-marshal.md) \] Wenn Ihre Anwendung [Pipes](/windows/desktop/Rpc/pipes) verwendet, müssen Sie die Option **/Oif** verwenden. Wenn Sie einen anderen Modus angeben, wechselt der MIDL-Compiler zu **/Oif.**

Um die Art und Weise zu optimieren, wie Ihr Stubcode gemarshallt wird, stellt Microsoft RPC ein \[ ACF-Optimierungsattribut [**bereit.**](optimize.md) \] Dieses Attribut wird als Schnittstellenattribut oder Vorgangsattribut verwendet, um den Marshallingmodus für einzelne Schnittstellen oder einzelne Vorgänge auszuwählen.

### <a name="calling-conventions"></a>Aufrufkonventionen

Stubs, die vom MIDL-Compiler in der interpretierten Methode mit den Schaltern **/Oi,** **/Oic** oder **/Oif** generiert werden, müssen während der C-Kompilierung entweder als stdcall- oder cdecl-Prozedur kompiliert werden. Eine PASCAL- oder Fastcall-Aufrufkonvention funktioniert nicht. Darüber hinaus muss der Serverstub als stdcall kompiliert werden.

## <a name="examples"></a>Beispiele

**midl /Oi filename.idl**

**midl /Oic filename.idl**

**midl /Oif filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**/no \_ robust**](-no-robust.md)
</dt> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**Optimieren**](optimize.md)
</dt> <dt>

[**/no \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 