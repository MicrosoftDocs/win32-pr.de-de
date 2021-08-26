---
title: Aufrufen einer Remoteprozedur
description: Sobald das Clientprogramm verteilter Anwendungen, das explizite Bindungshandles verwendet, über ein Bindungshandles verfügt, kann es Remoteverfahren ausführen.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Remoteprozeduraufruf RPC , Tasks, Ausführen eines Aufrufs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8218fd99e11c65f15dbbe7a56c2ece1b93720839498352d610312a0f66f95bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020080"
---
# <a name="making-a-remote-procedure-call"></a>Aufrufen einer Remoteprozedur

Sobald das Clientprogramm verteilter Anwendungen, das explizite Bindungshandles verwendet, über ein Bindungshandles verfügt, kann es Remoteverfahren ausführen.

Microsoft RPC bietet auch benutzerdefinierte Bindungshandles, implizite Bindungshandles und automatische Bindungshandles. Diese Bindungshandles bieten Client- und Serverprogrammen verschiedene Ebenen der Kontrolle über den Prozess der Ausführung von Remoteverfahren. Weitere Informationen zu verschiedenen Handletypen und deren Flexibilität finden Sie unter [Bindung und Handles.](binding-and-handles.md)

Um den Prozeduraufruf remote auszuführen, rufen Sie die clientseitige Stubfunktion auf die gleiche Weise auf, wie jede C-Funktion aufgerufen wird.

 

 




