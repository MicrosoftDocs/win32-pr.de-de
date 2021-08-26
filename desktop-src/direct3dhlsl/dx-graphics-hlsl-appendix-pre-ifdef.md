---
title: " ifdef- und ifndef-Direktiven"
description: Präprozessordirektiven, die bestimmen, ob eine bestimmte Präprozessorkonst constant oder ein Makro definiert ist.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef- und ifndef-Direktiven HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 584cde8856c48aeafed5665016a71146f8c2ffb341b837faa6bf35d627152c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068320"
---
# <a name="ifdef-and-ifndef-directives"></a>\#ifdef- und \# ifndef-Direktiven

Präprozessordirektiven, die bestimmen, ob eine bestimmte Präprozessorkonst constant oder ein Makro definiert ist.



| \#ifdef *identifier* ...  |
|---------------------------|
| \#endif                   |
| \#ifndef *identifier* ... |
| \#endif                   |



 

## <a name="parameters"></a>Parameter



| Element                                                                              | BESCHREIBUNG                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Bezeichner*<br/> | Bezeichner der zu überprüfenden Konstante oder des zu überprüfenden Makros. <br/> |



 

## <a name="remarks"></a>Hinweise

Sie können die \# ifdef- und \# ifndef-Direktiven [ \# ](dx-graphics-hlsl-appendix-pre-if.md) überall dort verwenden, wo der if verwendet werden kann. Die \# ifdef-Anweisung entspricht der -Direktive . Diese Anweisungen überprüfen nur das Vorhandensein oder Fehlen von Bezeichnern, die mit der [ \# define-Direktive](dx-graphics-hlsl-appendix-pre-define.md) definiert wurden, nicht auf Bezeichner, die im C- oder C++-Quellcode deklariert sind.

Diese Anweisungen werden nur bereitgestellt, um die Kompatibilität mit früheren Versionen der Sprache zu gewährleisten. Die Verwendung des definierten [Operators](dx-graphics-hlsl-appendix-pre-if.md) mit der \# if-Direktive wird bevorzugt.

Die \# ifndef-Direktive überprüft das Gegenteil der bedingung, die von \# ifdef überprüft wird. Wenn der Bezeichner nicht definiert ist, ist die Bedingung true (ungleich 0). Andernfalls ist die Bedingung false (null).

## <a name="examples"></a>Beispiele

Der Bezeichner kann von der Befehlszeile mithilfe der Option /D- übergeben werden. Bis zu 30 Makros können mit /D angegeben werden. Dies ist hilfreich, wenn überprüft werden soll, ob eine Definition vorhanden ist, da diese von der Befehlszeile übergeben werden kann. Im folgenden Beispiel wird dieses Verhalten verwendet, um zu bestimmen, ob eine Anwendung im Testmodus ausgeführt werden soll.


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



Bei der Kompilierung mit dem folgenden Befehl wird prog.cpp im Testmodus kompiliert. Andernfalls wird er im endgültigen Modus kompiliert.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#if, )](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





