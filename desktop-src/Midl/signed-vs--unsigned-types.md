---
title: Signierte und nicht signierte Typen (MIDL)
description: Erfahren Sie mehr über signierte und nicht signierte Typen in MIDL. Compiler, die unterschiedliche Standardtypen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- -Datentypen MIDL, signed und unsigned
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407383"
---
# <a name="signed-and-unsigned-types-midl"></a>Signierte und nicht signierte Typen (MIDL)

Compiler, die unterschiedliche Standardwerte für signierte und nicht signierte Typen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen. Sie können diese Probleme vermeiden, indem Sie Ihre Zeichentypen explizit als signiert oder nicht signiert deklarieren. Beachten Sie, dass DCE-IDL-Compiler das Schlüsselwort mit [**Vorzeichen**](signed.md)nicht erkennen. Daher ist dieses Feature nicht verfügbar, wenn Sie den MIDL-Compiler/osf-Switch verwenden.

MIDL definiert den [**kleinen**](small.md) Typ so, dass er das gleiche Standardzeichen wie der [**char-Typ**](char-idl.md) im C-Zielcompiler verwendet. Wenn der Compiler davon ausgeht, dass **char** nicht signiert ist, wird **small** auch als unsigned definiert. Mit vielen C-Compilern können Sie die Standardeinstellung als Befehlszeilenoption ändern. Beispielsweise ändert die Befehlszeilenoption **/J** in der Microsoft Visual C++ Entwicklungsumgebung das Standardzeichen von **char** von signed in unsigned.

Sie können auch das Vorzeichen von Variablen vom Typ [**char**](char-idl.md) und [**small**](small.md) mit dem MIDL-Compilerbefehlszeilenschalter [**/char**](-char.md)steuern. Mit diesem Schalter können Sie das Standardzeichen angeben, das vom Compiler verwendet wird. Der MIDL-Compiler deklariert explizit  das Vorzeichen aller char-Typen, die nicht mit ihrem C-Compilerstandardtyp in der generierten Headerdatei übereinstimmen.

 

 




