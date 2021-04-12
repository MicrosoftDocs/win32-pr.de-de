---
title: Basistypen
description: Um die Probleme zu vermeiden, die von der Implementierung abhängigen Datentypen auf unterschiedlichen Computerarchitekturen verursacht werden können, definiert das Mittel l seine eigenen Basis Datentypen.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316244"
---
# <a name="base-types"></a>Basistypen

Um die Probleme zu vermeiden, die von der Implementierung abhängigen Datentypen auf unterschiedlichen Computerarchitekturen verursacht werden können, definiert das Mittel l seine eigenen Basis Datentypen.



| Basistyp                         | BESCHREIBUNG                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**boolean**](/windows/desktop/Midl/boolean)       | Ein Datenelement, das den Wert **true** oder **false** aufweisen kann.                                                                                                          |
| [**Hobby**](/windows/desktop/Midl/byte)             | Ein 8-Bit-Datenelement, das ohne Änderung garantiert übertragen wird.                                                                                                 |
| [**Char**](/windows/desktop/Midl/char-idl)         | Ein 8-Bit-Datenelement ohne Vorzeichen.                                                                                                                              |
| [**Maß**](/windows/desktop/Midl/double)         | Eine 64-Bit-Gleit Komma Zahl.                                                                                                                                     |
| [**Hafen**](/windows/desktop/Midl/float)           | Eine 32-Bit-Gleit Komma Zahl.                                                                                                                                     |
| [**Handle \_ t**](/windows/desktop/Midl/handle-t)    | Ein Primitives handle, das für die RPC-Bindung oder das Serialisieren von Daten verwendet werden kann.                                                                                            |
| [**Hyper**](/windows/desktop/Midl/hyper)           | Eine 64-Bit-Ganzzahl, die als " [**Signed**](/windows/desktop/Midl/signed) " oder " [**Ganzzahl ohne Vorzeichen**](/windows/desktop/Midl/unsigned) " deklariert werden kann, kann auch als " **\_ Int64**" bezeichnet werden.                  |
| [**INT**](/windows/desktop/Midl/int)               | Eine 32-Bit-Ganzzahl, die als " **Signed** " oder " **Ganzzahl ohne Vorzeichen**" deklariert werden kann.                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Ein Schlüsselwort, das einen ganzzahligen Typ mit 32-Bit-oder 64-Bit-Eigenschaften angibt.                                                                              |
| [**lange**](/windows/desktop/Midl/long)             | Ein Modifizierer für **int** , der eine 32-Bit-Ganzzahl angibt. Kann als " **Signed** " oder " **Ganzzahl ohne Vorzeichen**" deklariert werden.                                                       |
| [**short**](/windows/desktop/Midl/short)           | Eine 16-Bit-Ganzzahl, die als " **Signed** " oder " **Ganzzahl ohne Vorzeichen**" deklariert werden kann.                                                                                         |
| [**zuletzt**](/windows/desktop/Midl/small)           | Ein Modifizierer für **int** , der eine 8-Bit-Ganzzahl angibt. Kann als " **Signed** " oder " **Ganzzahl ohne Vorzeichen**" deklariert werden.                                                       |
| [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)      | Breit Zeichentyp, der als Microsoft-Erweiterung für IDL unterstützt wird. Daher ist dieser Typ nicht verfügbar, wenn Sie die Kompilierung mit dem [ / **eines Zertifikats**](/windows/desktop/Midl/-osf) -Schalter durchsetzen. |



 

Die Header Datei Rpcndr. h stellt Definitionen für die meisten dieser Basis Datentypen bereit. Das Schlüsselwort " **int** " wird erkannt und ist auf 32-Bit-Plattformen transaktionabel. Auf 16-Bit-Plattformen ist für den **int** -Datentyp ein Modifizierer, z. b. **Short** oder **Long**, erforderlich, um seine Länge anzugeben.

Obwohl **void \* \*** als generischer Zeigertyp durch den ANSI C-Standard erkannt wird, schränkt die Verwendung durch die Mittel l ein. Jeder Zeiger, der in einem Remote-oder Serialisierungsvorgang verwendet wird, muss auf Basis Typen oder auf Typen verweisen, die aus Basis Typen erstellt werden. (Es gibt eine Ausnahme: Kontext Handles werden als **void** -Typen definiert. Weitere Informationen finden Sie unter [Kontext Handles](context-handles.md).)

 

 