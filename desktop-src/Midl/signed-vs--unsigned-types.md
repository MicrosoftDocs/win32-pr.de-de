---
title: Signierte und nicht signierte Typen (MIDL)
description: Erfahren Sie mehr über signierte und nicht signierte Typen in MIDL. Compiler, die verschiedene Standardtypen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- Datentypen MIDL , signiert und nicht signiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9f65931720e80de6575d8b7125e6b5082a32e510e1be07e620e6592d30e485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066750"
---
# <a name="signed-and-unsigned-types-midl"></a>Signierte und nicht signierte Typen (MIDL)

Compiler, die unterschiedliche Standardwerte für signierte und nicht signierte Typen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen. Sie können diese Probleme vermeiden, indem Sie Ihre Zeichentypen explizit als signiert oder unsigniert deklarieren. Beachten Sie, dass DCE-IDL-Compiler das schlüsselwort signed nicht [**erkennen.**](signed.md) Daher ist dieses Feature nicht verfügbar, wenn Sie den **MIDL-Compiler/osf-Switch** verwenden.

MIDL definiert den [**kleinen Typ,**](small.md) um das gleiche Standardzeichen wie der [**char-Typ**](char-idl.md) im C-Zielcompiler zu verwenden. Wenn der Compiler an nimmt, **dass char** nicht signiert ist, **wird small** auch als unsigned definiert. Mit vielen C-Compilern können Sie den Standardwert als Befehlszeilenoption ändern. Beispielsweise ändert die Befehlszeilenoption **/J** in Microsoft Visual C++-Entwicklungsumgebung das Standardzeichen von **char** von signed in unsigned.

Sie können auch das Vorzeichen von Variablen vom Typ [**char**](char-idl.md) und [**small mit**](small.md) dem MIDL-Compilerbefehlszeilenschalter [**/char steuern.**](-char.md) Mit diesem Schalter können Sie das Standardzeichen angeben, das vom Compiler verwendet wird. Der MIDL-Compiler deklariert explizit das  Vorzeichen aller char-Typen, die nicht mit dem C-Compiler-Standardtyp in der generierten Headerdatei übereinstimmen.

 

 




