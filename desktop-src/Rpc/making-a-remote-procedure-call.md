---
title: Ausführen eines Remote Prozedur Aufrufes
description: Sobald das Client Programm verteilter Anwendungen, die explizite Bindungs Handles verwenden, über ein Bindungs Handle verfügt, kann es Remote Prozeduren ausführen.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Anrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707182"
---
# <a name="making-a-remote-procedure-call"></a>Ausführen eines Remote Prozedur Aufrufes

Sobald das Client Programm verteilter Anwendungen, die explizite Bindungs Handles verwenden, über ein Bindungs Handle verfügt, kann es Remote Prozeduren ausführen.

Microsoft RPC bietet auch benutzerdefinierte Bindungs Handles, implizite Bindungs Handles und automatische Bindungs Handles. Diese Bindungs Handles bieten Client-und Serverprogrammen verschiedene Steuerungs Ebenen für das Ausführen von Remote Prozeduren. Ausführliche Informationen zu verschiedenen handle-Typen und der von Ihnen angebotenen Flexibilität finden Sie unter [Bindung und Handles](binding-and-handles.md).

Um den Prozedur Aufruf Remote auszuführen, müssen Sie die Client seitige Stub-Funktion auf die gleiche Weise aufrufen, wie jede C-Funktion aufgerufen wird.

 

 




