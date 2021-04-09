---
title: Typserialisierung
description: Der mittlerer l-Compiler generiert bis zu drei Funktionen für jeden Typ, auf den das Attribut \ codieren \ oder \ Decode \ angewendet wird.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674617bc98c92dbc684a29d1a3c91ac6a7429e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101943"
---
# <a name="type-serialization"></a>Typserialisierung

Der mittlerer l-Compiler generiert bis zu drei Funktionen für jeden Typ, auf den das \[ Attribut [Codieren](/windows/desktop/Midl/encode) \] oder \[ [decodieren](/windows/desktop/Midl/decode) \] angewendet wird. Für einen benutzerdefinierten Typ mit dem Namen " *MyType*" generiert der Compiler z. b. Code für die Funktionen "MyType \_ encode", "MyType \_ Decode" und "MyType \_ alignsize". Für diese Funktionen schreibt der Compiler Prototypen in Stub. h und Quellcode in den Stub \_ c.c.. Im Allgemeinen können Sie ein *MyType* -Objekt mit MyType codieren \_ und ein Objekt mithilfe von MyType decodieren aus dem Puffer decodieren \_ . MyType \_ alignsize wird verwendet, wenn Sie die Größe des marshallingpuffers kennen müssen, bevor Sie ihn zuordnen.

Die folgende Codierungsfunktion wird vom-Mittell-Compiler generiert. Diese Funktion serialisiert die Daten für das Objekt, auf das pObject verweist, und der Puffer wird gemäß der im handle angegebenen Methode abgerufen. Nachdem Sie die serialisierten Daten in den Puffer geschrieben haben, Steuern Sie den Puffer. Beachten Sie, dass das Handle den Status von den vorherigen Aufrufen erbt, und die Puffer müssen bei 8 ausgerichtet werden.

Für ein implizites handle:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Für ein explizites handle:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

Die folgende Funktion deserialisiert die Daten aus dem Speicher der Anwendung in das Objekt, auf das von pObject verwiesen wird. Sie geben einen gemarshallten Puffer gemäß der im handle angegebenen Methode an. Beachten Sie, dass das Handle den Status von den vorherigen Aufrufen erben kann und die Puffer bei 8 ausgerichtet werden müssen.

Für ein implizites handle:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Für ein explizites handle:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

Die folgende Funktion gibt eine Größe (in Bytes) zurück, die die Typinstanz zuzüglich der zum Ausrichten der Daten benötigten Füll Zeichen enthält. Dies ermöglicht die Serialisierung eines Satzes von Instanzen desselben oder unterschiedlicher Typen in einen Puffer, wobei sichergestellt wird, dass die Daten für jedes Objekt entsprechend ausgerichtet werden. MyType \_ alignsize geht davon aus, dass die Instanz, auf die von pObject verwiesen wird, in einen Puffer gemarshallt wird, beginnend bei dem mit 8 ausgerichteten Offset.

Für ein implizites handle:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Für ein explizites handle:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Beachten Sie, dass bei beiden Remote Prozeduren mit impliziten Bindungs Handles und serialisierten Typen mit impliziten serialisierungshandles dieselbe globale handle-Variable verwendet wird. Daher empfiehlt es sich, die Typserialisierung und Remote Prozeduren in einer Schnittstelle mit impliziten Handles nicht zu mischen. Weitere Informationen finden Sie unter [implizite und explizite Handles](implicit-versus-explicit-handles.md).

 

 