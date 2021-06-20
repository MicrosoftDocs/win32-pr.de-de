---
title: Signierte und nicht signierte Typen (RPC)
description: Erfahren Sie mehr über signierte und nicht signierte Typen in RPC. Compiler, die unterschiedliche Standardtypen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406543"
---
# <a name="signed-and-unsigned-types-rpc"></a>Signierte und nicht signierte Typen (RPC)

Compiler, die unterschiedliche Standardwerte für signierte und nicht signierte Typen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen. Sie können diese Probleme vermeiden, indem Sie Ihre Zeichentypen explizit als **signiert** oder nicht signiert **deklarieren.**

MIDL definiert den [**kleinen**](/windows/desktop/Midl/small) Typ so, dass er das gleiche Standardzeichen wie der **char-Typ** im C-Zielcompiler verwendet. Wenn der Compiler davon ausgeht, dass **char** nicht signiert ist, wird **small** auch als unsigned definiert. Mit vielen C-Compilern können Sie die Standardeinstellung als Befehlszeilenoption ändern. Beispielsweise ändert die Befehlszeilenoption des Microsoft C-Compilers **/J** das Standardzeichen von **char** von signed in unsigned.

Sie können auch das Vorzeichen von Variablen vom Typ **char** und **small** mit dem MIDL-Compilerbefehlszeilenschalter [**/char**](/windows/desktop/Midl/-char)steuern. Mit diesem Schalter können Sie das Standardzeichen angeben, das vom Compiler verwendet wird. Der MIDL-Compiler deklariert explizit  das Vorzeichen aller char-Typen, die nicht mit Ihrem C-Compiler-Standardtyp in der generierten Headerdatei übereinstimmen.

 

 
