---
description: Der imm enthält eine Thread Identifikations Überprüfung, mit der bestimmt wird, ob ein aufrufenden Thread der Ersteller eines angegebenen Eingabemethoden-Kontext Handles (himc-Typs) oder Fenster Handles (HWND-Typ) ist.
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Entwickeln IME-Aware Anwendungen mit mehreren Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351482"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Entwickeln IME-Aware Anwendungen mit mehreren Threads

Der imm enthält eine Thread Identifikations Überprüfung, mit der bestimmt wird, ob ein aufrufenden Thread der Ersteller eines angegebenen Eingabemethoden-Kontext Handles (himc-Typs) oder Fenster Handles (HWND-Typ) ist. Wenn der Thread nicht der Ersteller des Handles ist, tritt bei der aufgerufenen imm-Funktion ein Fehler auf, und ein nachfolgende Aufruf von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen \_ ungültigen \_ Zugriff zurück.

> [!Note]  
> Die aktuelle imm-Architektur bietet keine Synchronisierungs Funktion für den Zugriff auf die imm-Handles.

 

Um die Überprüfung der Thread Identifizierung verwenden zu können, müssen die Anwendungen die folgenden Richtlinien einhalten:

-   Ein Thread sollte nicht auf den von einem anderen Thread erstellten Eingabe Kontext zugreifen.
-   Ein Thread sollte einem von einem anderen Thread erstellten Fenster keinen Eingabe Kontext zuordnen und umgekehrt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Eingabemethoden-Managers](using-input-method-manager.md)
</dt> </dl>

 

 
