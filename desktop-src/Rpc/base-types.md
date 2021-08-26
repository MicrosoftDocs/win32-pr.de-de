---
title: Basistypen
description: Um probleme zu vermeiden, die implementierungsabhängige Datentypen in verschiedenen Computerarchitekturen verursachen können, definiert MIDL eigene Basisdatentypen.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aadc1ae5fedd73a01ce0fd7ed735689e043cff0d74910175cf2ab691c22eeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023280"
---
# <a name="base-types"></a>Basistypen

Um probleme zu vermeiden, die implementierungsabhängige Datentypen in verschiedenen Computerarchitekturen verursachen können, definiert MIDL eigene Basisdatentypen.



| Basistyp                         | BESCHREIBUNG                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**boolean**](/windows/desktop/Midl/boolean)       | Ein Datenelement, das den Wert **TRUE** oder **FALSE haben kann.**                                                                                                          |
| [**Byte**](/windows/desktop/Midl/byte)             | Ein 8-Bit-Datenelement, das garantiert ohne Änderungen übertragen wird.                                                                                                 |
| [**Char**](/windows/desktop/Midl/char-idl)         | Ein 8-Bit-Datenelement ohne Vorzeichen.                                                                                                                              |
| [**Doppel**](/windows/desktop/Midl/double)         | Eine 64-Bit-Gleitkommazahl.                                                                                                                                     |
| [**schweben**](/windows/desktop/Midl/float)           | Eine 32-Bit-Gleitkommazahl.                                                                                                                                     |
| [**handle \_ t**](/windows/desktop/Midl/handle-t)    | Ein primitives Handle, das für die RPC-Bindung oder datenserialisierung verwendet werden kann.                                                                                            |
| [**Hyper**](/windows/desktop/Midl/hyper)           | Eine 64-Bit-Ganzzahl, die [](/windows/desktop/Midl/signed) entweder [](/windows/desktop/Midl/unsigned) mit Vorzeichen oder ohne Vorzeichen deklariert werden kann, kann auch als **\_ int64 bezeichnet werden.**                  |
| [**INT**](/windows/desktop/Midl/int)               | Eine 32-Bit-Ganzzahl, die  als mit oder ohne **Vorzeichen deklariert werden kann.**                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Ein Schlüsselwort, das einen integralen Typ angibt, der entweder über 32-Bit- oder 64-Bit-Eigenschaften verfügt.                                                                              |
| [**long**](/windows/desktop/Midl/long)             | Ein Modifizierer **für int,** der eine 32-Bit-Ganzzahl angibt. Kann als mit **oder** ohne **Vorzeichen deklariert werden.**                                                       |
| [**short**](/windows/desktop/Midl/short)           | Eine 16-Bit-Ganzzahl, die  als mit oder ohne **Vorzeichen deklariert werden kann.**                                                                                         |
| [**klein**](/windows/desktop/Midl/small)           | Ein Modifizierer **für int,** der eine 8-Bit-Ganzzahl angibt. Kann als mit **oder** ohne **Vorzeichen deklariert werden.**                                                       |
| [**wchar \_ t**](/windows/desktop/Midl/wchar-t)      | Breitzeichentyp, der als Microsoft-Erweiterung für IDL unterstützt wird. Daher ist dieser Typ nicht verfügbar, wenn Sie mit dem [ / **Osf-Switch kompilieren.**](/windows/desktop/Midl/-osf) |



 

Die Headerdatei Rpcndr.h enthält Definitionen für die meisten dieser Basisdatentypen. Das Schlüsselwort **int** wird erkannt und kann auf 32-Bit-Plattformen übertragen werden. Auf 16-Bit-Plattformen erfordert der **int-Datentyp** einen Modifizierer, z. B. **short** oder **long,** um seine Länge anzugeben.

Obwohl **\* \* void** vom ANSI C-Standard als generischer Zeigertyp erkannt wird, schränkt MIDL seine Verwendung ein. Jeder Zeiger, der in einem Remote- oder Serialisierungsvorgang verwendet wird, muss entweder auf Basistypen oder auf Typen verweisen, die aus Basistypen erstellt wurden. (Es gibt eine Ausnahme: Kontexthandles werden als **void-Typen** definiert. Weitere Informationen finden Sie unter [Kontexthandles](context-handles.md).)

 

 