---
title: Typserialisierung
description: Der MIDL-Compiler generiert bis zu drei Funktionen für jeden Typ, auf den das Attribut \encode\ oder \decode\ angewendet wird.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d898a077ff55bb03a76fbd7579e28a8bcdf18c792330b32b1eb832c6b9058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011098"
---
# <a name="type-serialization"></a>Typserialisierung

Der MIDL-Compiler generiert bis zu drei Funktionen für jeden Typ, auf den \[ [das Codierungs- oder](/windows/desktop/Midl/encode) \] \[ [Decodierungsattribut](/windows/desktop/Midl/decode) angewendet \] wird. Für einen benutzerdefinierten Typ namens *MyType* generiert der Compiler beispielsweise Code für die Funktionen MyType \_ Encode, MyType Decode und \_ MyType \_ AlignSize. Für diese Funktionen schreibt der Compiler Prototypen in Stub.h und Quellcode in Stub \_ c.c. Im Allgemeinen können Sie ein *MyType-Objekt* mit MyType codieren und ein Objekt mithilfe von MyType Decode aus dem \_ Puffer \_ decodieren. MyType AlignSize wird verwendet, wenn Sie die Größe des Marshallingpuffers kennen müssen, \_ bevor Sie ihn zuordnen.

Die folgende Codierungsfunktion wird vom MIDL-Compiler generiert. Diese Funktion serialisiert die Daten für das Objekt, auf das pObject zeigt, und der Puffer wird gemäß der im Handle angegebenen Methode erhalten. Nachdem Sie die serialisierten Daten in den Puffer geschrieben haben, steuern Sie den Puffer. Beachten Sie, dass das Handle den Status der vorherigen Aufrufe erbt und die Puffer auf 8 ausgerichtet werden müssen.

Für ein implizites Handle:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Für ein explizites Handle:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

Die folgende Funktion deserialisiert die Daten aus dem Anwendungsspeicher in das Objekt, auf das pObject zeigt. Sie geben einen gemarshallten Puffer entsprechend der im Handle angegebenen Methode an. Beachten Sie, dass das Handle den Status der vorherigen Aufrufe erben kann und die Puffer auf 8 ausgerichtet werden müssen.

Für ein implizites Handle:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Für ein explizites Handle:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

Die folgende Funktion gibt eine Größe in Bytes zurück, die die Typinstanz sowie alle Auf padding-Bytes enthält, die zum Ausrichten der Daten erforderlich sind. Dies ermöglicht das Serialisieren einer Reihe von Instanzen desselben oder verschiedener Typen in einen Puffer, während gleichzeitig sichergestellt wird, dass die Daten für jedes Objekt entsprechend ausgerichtet sind. MyType AlignSize geht davon aus, dass die Instanz, auf die pObject zeigt, in einen Puffer gemarshallt wird, beginnend am Offset, der bei \_ 8 ausgerichtet ist.

Für ein implizites Handle:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Für ein explizites Handle:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Beachten Sie, dass sowohl Remoteverfahren mit impliziten Bindungshandles als auch serialisierte Typen mit impliziten Serialisierungshandles dieselbe globale Handlevariable verwenden. Daher ist es ratsam, die Typserialisierung und Remoteverfahren nicht in einer Schnittstelle mit impliziten Handles zu mischen. Weitere Informationen finden Sie unter [Implizite und explizite Handles.](implicit-versus-explicit-handles.md)

 

 