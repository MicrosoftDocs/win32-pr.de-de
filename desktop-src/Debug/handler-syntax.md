---
description: In diesem Abschnitt werden die Syntax und die Verwendung der strukturierten Ausnahmebehandlung beschrieben, die im Microsoft C/C++-Optimierungs Compiler implementiert ist. Die folgenden Schlüsselwörter werden vom Compiler als Teil des strukturierten Mechanismus zur Ausnahmebehandlung interpretiert.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: HandlerSyntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860680"
---
# <a name="handler-syntax"></a>HandlerSyntax

In diesem Abschnitt werden die Syntax und die Verwendung der strukturierten Ausnahmebehandlung beschrieben, die im Microsoft C/C++-Optimierungs Compiler implementiert ist. Die folgenden Schlüsselwörter werden vom Compiler als Teil des strukturierten Mechanismus zur Ausnahmebehandlung interpretiert.



| Schlüsselwort         | BESCHREIBUNG                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_versu**     | Beginnt einen überwachten Code Körper. Wird mit dem Schlüsselwort **\_ \_ außer** verwendet, um einen [Ausnahmehandler](exception-handler-syntax.md)zu erstellen, oder mit dem Schlüsselwort " **\_ \_ endgültig** " zum Erstellen eines Beendigungs [Handlers](termination-handler-syntax.md) |
| **\_\_davon**  | Startet einen Codeblock, der nur ausgeführt wird, wenn eine Ausnahme innerhalb des zugeordneten **\_ \_ try** -Blocks auftritt.                                                                                                                                   |
| **\_\_finally** | Startet einen Codeblock, der ausgeführt wird, wenn die Ablauf Steuerung den zugeordneten **\_ \_ try** -Block verlässt.                                                                                                                                    |
| **\_\_lassen Sie**   | Ermöglicht das sofortige Beenden des **\_ \_ try** -Blocks, ohne dass eine nicht ordnungsgemäße Beendigung und die Leistungseinbußen verursacht werden.                                                                                                                      |



 

Der Compiler interpretiert außerdem die Funktionen [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)und [**abnormalabbruch**](abnormaltermination.md) als Schlüsselwörter, und ihre Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler. Im folgenden finden Sie eine kurze Beschreibung dieser Funktionen.



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Gibt einen Code zurück, der den Typ der Ausnahme identifiziert. Diese Funktion kann nur innerhalb des Filter Ausdrucks oder des ausnahmehandlerblocks aufgerufen werden.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Gibt einen Zeiger auf eine [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Struktur zurück, die Zeiger auf den Kontext Daten Satz und den Ausnahme Daten Satz enthält. Diese Funktion kann nur innerhalb des Filter Ausdrucks eines Ausnahme Handlers aufgerufen werden. |
| [**AbnormalTermination**](abnormaltermination.md)         | Gibt an, ob die Ablauf Steuerung den zugeordneten **\_ \_ try** -Block nacheinander nach dem Ausführen der letzten Anweisung im-Block verlassen hat. Diese Funktion kann nur innerhalb des **\_ \_ letzten Blocks eines** Beendigungs Handlers aufgerufen werden.              |



 

 

 



