---
title: Signierte und nicht signierte Typen (RPC)
description: Erfahren Sie mehr über signierte und nicht signierte Typen in RPC. Compiler, die verschiedene Standardtypen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17a2ccf28233bb14e0811e8015c83aede37d60c58fe9411f13806355fdb7f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017699"
---
# <a name="signed-and-unsigned-types-rpc"></a>Signierte und nicht signierte Typen (RPC)

Compiler, die unterschiedliche Standardwerte für signierte und nicht signierte Typen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen. Sie können diese Probleme vermeiden, indem Sie Ihre Zeichentypen explizit als mit **oder** **ohne Vorzeichen deklarieren.**

MIDL definiert den [**kleinen Typ,**](/windows/desktop/Midl/small) um das gleiche Standardzeichen wie der **char-Typ** im C-Zielcompiler zu verwenden. Wenn der Compiler an nimmt, **dass char** nicht signiert ist, **wird small** auch als unsigned definiert. Mit vielen C-Compilern können Sie den Standardwert als Befehlszeilenoption ändern. Beispielsweise ändert die Befehlszeilenoption Microsoft C compiler **/J** das Standardzeichen **von char** von signed in unsigned.

Sie können auch das Vorzeichen von Variablen vom Typ **char** und **small mit** dem MIDL-Compilerbefehlszeilenschalter [**/char steuern.**](/windows/desktop/Midl/-char) Mit diesem Schalter können Sie das Standardzeichen angeben, das vom Compiler verwendet wird. Der MIDL-Compiler deklariert explizit das  Vorzeichen aller char-Typen, die nicht mit dem C-Compiler-Standardtyp in der generierten Headerdatei übereinstimmen.

 

 
