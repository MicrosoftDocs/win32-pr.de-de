---
title: " ifdef-und ifndef-Direktiven"
description: Präprozessordirektiven, die bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef-und ifndef-Direktiven HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037990"
---
# <a name="ifdef-and-ifndef-directives"></a>\#ifdef-und \# ifndef-Direktiven

Präprozessordirektiven, die bestimmen, ob eine bestimmte präprozessorkonstante oder ein bestimmtes Makro definiert ist.



| \#ifdef- *Bezeichner* ...  |
|---------------------------|
| \#endif                   |
| \#ifndef- *Bezeichner* ... |
| \#endif                   |



 

## <a name="parameters"></a>Parameter



| Element                                                                              | BESCHREIBUNG                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Figur*<br/> | Der Bezeichner der zu überprüfen Konstanten oder Makros. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie können die \# ifdef-und \# ifndef-Direktiven überall [ \# ](dx-graphics-hlsl-appendix-pre-if.md) dort verwenden, wo verwendet werden kann. Die \# ifdef-Anweisung entspricht der-Direktive. Diese Direktiven überprüfen nur das vorhanden sein oder Fehlen von [ \# bezeichlen](dx-graphics-hlsl-appendix-pre-define.md) , die mithilfe der define-Direktive definiert wurden, nicht für Bezeichner, die im C-oder C++-Quellcode deklariert sind.

Diese Anweisungen werden nur bereitgestellt, um die Kompatibilität mit früheren Versionen der Sprache zu gewährleisten. Die Verwendung des [definierten](dx-graphics-hlsl-appendix-pre-if.md) Operators mit der \# if-Direktive wird bevorzugt.

Die \# ifndef-Direktive prüft das Gegenteil der von \# ifdef geprüften Bedingung. Wenn der Bezeichner nicht definiert ist, ist die Bedingung "true" (ungleich 0); Andernfalls ist die Bedingung "false" (null).

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



Bei der Kompilierung mit dem folgenden Befehl wird "PROG. cpp" im Testmodus kompiliert. Andernfalls wird es im abschließenden Modus kompiliert.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessordirektiven (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Wenn,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





