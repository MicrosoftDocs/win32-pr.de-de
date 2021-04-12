---
description: Der ergänzte Symbol Name enthält Zeichen, die unterscheiden, wie ein öffentliches Symbol deklariert wurde.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Ergänzte Symbol Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482731"
---
# <a name="decorated-symbol-names"></a>Ergänzte Symbol Namen

Der ergänzte Symbol Name enthält Zeichen, die unterscheiden, wie ein öffentliches Symbol deklariert wurde. Für \_ \_ StdCall-Funktionen enthalten Namen das Zeichen "@" und eine Dezimalzahl, die die Anzahl von Bytes in den Funktionsparametern angibt. Der ergänzte Name der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion lautet z. b LoadLibrary@4 .. Für C++-Funktionen ist die namens Ergänzung komplexer und unterscheidet sich von Compiler zu Compiler.

Um den nicht ergänzten Symbolnamen abzurufen, verwenden Sie die [**undecoratesymbolname**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) -Funktion. Sie können auch die [**symabtoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion aufzurufen, um anzufordern, dass der Symbol Handler immer Symbole mit nicht ergänzten Namen vorhanden ist. Sie müssen diese Option vor dem Laden der Symbole festlegen, da der Symbol Handler die Symbol namens Tabellen zur Ladezeit erstellt.

 

 
