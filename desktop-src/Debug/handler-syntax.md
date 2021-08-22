---
description: In diesem Abschnitt wird die Syntax und Verwendung der strukturierten Ausnahmebehandlung beschrieben, die im Microsoft C/C++-Optimierungscompiler implementiert ist. Die folgenden Schlüsselwörter werden vom Compiler als Teil des strukturierten Ausnahmebehandlungsmechanismus interpretiert.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Handlersyntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5171a1de095faa0c3362a7998903d31f90eb630e51c5ec16e7e77d467117715c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260610"
---
# <a name="handler-syntax"></a>Handlersyntax

In diesem Abschnitt wird die Syntax und Verwendung der strukturierten Ausnahmebehandlung beschrieben, die im Microsoft C/C++-Optimierungscompiler implementiert ist. Die folgenden Schlüsselwörter werden vom Compiler als Teil des strukturierten Ausnahmebehandlungsmechanismus interpretiert.



| Stichwort         | BESCHREIBUNG                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_try**     | Startet einen wächter Code. Wird mit dem **\_ \_ except-Schlüsselwort** verwendet, um einen [Ausnahmehandler zu erstellen,](exception-handler-syntax.md)oder mit dem **\_ \_ finally-Schlüsselwort,** um einen [Beendigungshandler zu erstellen.](termination-handler-syntax.md) |
| **\_\_Außer**  | Startet einen Codeblock, der nur ausgeführt wird, wenn eine Ausnahme innerhalb des zugeordneten **\_ \_ try-Blocks auftritt.**                                                                                                                                   |
| **\_\_finally** | Startet einen Codeblock, der ausgeführt wird, wenn der Ablauf der Steuerung den zugeordneten **\_ \_ try-Block verlässt.**                                                                                                                                    |
| **\_\_Verlassen**   | Ermöglicht die sofortige Beendigung des **\_ \_ try-Blocks,** ohne dass eine ungewöhnliche Beendigung und leistungsbehaftete Leistung verursacht wird.                                                                                                                      |



 

Der Compiler interpretiert auch die [**Funktionen GetExceptionCode,**](getexceptioncode.md) [**GetExceptionInformation**](getexceptioninformation.md)und [**AbnormalTermination**](abnormaltermination.md) als Schlüsselwörter, und ihre Verwendung außerhalb der entsprechenden Ausnahmebehandlungssyntax generiert einen Compilerfehler. Im Folgenden finden Sie kurze Beschreibungen dieser Funktionen.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Gibt einen Code zurück, der den Typ der Ausnahme identifiziert. Diese Funktion kann nur innerhalb des Filterausdrucks oder des Ausnahmehandlerblocks aufgerufen werden.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Gibt einen Zeiger auf eine [**EXCEPTION \_ POINTERS-Struktur**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) zurück, die Zeiger auf den Kontextdatensatz und den Ausnahmedatensatz enthält. Diese Funktion kann nur innerhalb des Filterausdrucks eines Ausnahmehandlers aufgerufen werden. |
| [**AbnormalTermination**](abnormaltermination.md)         | Gibt an, ob der Ablauf der Steuerung den zugeordneten **\_ \_ try-Block** sequenziell verlassen hat, nachdem die letzte Anweisung im -Block ausgeführt wurde. Diese Funktion kann nur innerhalb des **\_ \_ finally-Blocks** eines Beendigungshandlers aufgerufen werden.              |



 

 

 



