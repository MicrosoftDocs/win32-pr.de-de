---
title: /Cpp_opt Schalter
description: Der \_ Schalter/cpp opt gibt Optionen an, die an den C/C++-Präprozessor übergeben werden.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /Cpp_opt-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104391285"
---
# <a name="cpp_opt-switch"></a>/cpp \_ opt-Schalter

Der Schalter **/cpp \_ opt** gibt Optionen an, die an den C/C++-Präprozessor übergeben werden.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*C- \_ \_ Präprozessoroption* 
</dt> <dd>

Gibt die Befehlszeilenoption an, die dem aufgerufenen Präprozessor zugeordnet ist. 

**Hinweis**: für die Microsoft c/C++-Präprozessoren müssen Sie den `/E` Schalter als Teil der *c- \_ präprozessoroptionszeichenfolge \_* angeben. 

Anführungszeichen sind erforderlich, wenn mehr als eine Option und Leerzeichen verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diesen Switch nur, wenn es einen bestimmten Grund dafür gibt. Wichtige Informationen zur Vorverarbeitung finden Sie unter [C-präprozessoranforderungen für Mittel l](c-preprocessor-requirements-for-midl.md) .

Der Schalter " **/cpp \_ opt** " kann mit oder ohne den Schalter " [**/cpp \_ cmd**](-cpp-cmd.md) " verwendet werden. Weitere Informationen zur Erstellung der präprozessorbefehlszeile in beiden Fällen finden Sie unter **/cpp \_ cmd** .

Der **/cpp \_ opt** -Schalter muss, falls angegeben, immer enthalten, um `/E` ordnungsgemäß zu funktionieren.

## <a name="examples"></a>Beispiele

**Mittel l/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**

**Mittel l/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**

**Mittel l/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**

**Mittel l/cpp \_ cmd "CL"/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp- \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/No \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[C-präprozessoranforderungen für die Mittel l](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




