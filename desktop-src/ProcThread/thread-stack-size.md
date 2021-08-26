---
description: Jeder neue Thread oder jede neue Fiber erhält einen eigenen Stapelspeicher, der sowohl aus reservierten als auch aus ursprünglich ausgeführten Arbeitsspeicher besteht.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Threadstapelgröße
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff392577d529ab03a3859a0c6b0a94057ff8d8e0dc3c09fef86176d5c8950ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031410"
---
# <a name="thread-stack-size"></a>Threadstapelgröße

Jeder neue Thread oder jede neue Fiber erhält einen eigenen Stapelspeicher, der sowohl aus reservierten als auch aus ursprünglich ausgeführten Arbeitsspeicher besteht. Die Größe des reservierten Arbeitsspeichers stellt die gesamte Stapelzuordnung im virtuellen Arbeitsspeicher dar. Daher ist die reservierte Größe auf den virtuellen Adressbereich beschränkt. Die seiten, für die ursprünglich ein Commit ausgeführt wurde, nutzen keinen physischen Speicher, bis auf sie verwiesen wird. Sie entfernen jedoch Seiten aus dem Commitlimit des Systems, d. h. der Größe der Seitendatei und der Größe des physischen Arbeitsspeichers. Das System führt bei Bedarf einen Commit für zusätzliche Seiten aus dem reservierten Stapelspeicher durch, bis entweder der Stapel die reservierte Größe minus einer Seite erreicht (die als Schutzseite verwendet wird, um Stapelüberlauf zu verhindern), oder das System so wenig Arbeitsspeicher hat, dass der Vorgang fehlschlägt.

Es empfiehlt sich, eine möglichst kleine Stapelgröße auszuwählen und den Stapel zu committen, der benötigt wird, damit der Thread oder die Fiber zuverlässig ausgeführt werden kann. Jede Seite, die für den Stapel reserviert ist, kann nicht für andere Zwecke verwendet werden.

Ein Stapel wird freigegeben, wenn sein Thread beendet wird. Sie wird nicht freigegeben, wenn der Thread von einem anderen Thread beendet wird.

Die Standardgröße für den reservierten und anfänglich ausgeführten Stapelspeicher wird im Header der ausführbaren Datei angegeben. Die Thread- oder Fibererstellung schlägt fehl, wenn nicht genügend Arbeitsspeicher vorhanden ist, um die Anzahl der angeforderten Bytes zu reservieren oder zu committen. Die standard vom Linker verwendete Stapelreservierungsgröße beträgt 1 MB. Um eine andere Standardgröße für die Stapelreservierung für alle Threads und Fibers anzugeben, verwenden Sie die STACKSIZE-Anweisung in der Moduldefinitionsdatei (DEF). Das Betriebssystem rundet die angegebene Größe auf das nächste Vielfache der Zuordnungsgranularität des Systems auf (in der Regel 64 KB). Verwenden Sie die [**GetSystemInfo-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) um die Zuordnungsgranularität des aktuellen Systems abzurufen.

Verwenden Sie den *dwStackSize-Parameter* der [**CreateThread-,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**CreateRemoteThread-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)oder [**CreateFiber-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-createfiber) um den ursprünglich ausgeführten Stapelspeicher zu ändern. Dieser Wert wird auf die nächste Seite aufgerundet. Im Allgemeinen ist die Reservegröße die Standardreservegröße, die im ausführbaren Header angegeben ist. Wenn die anfänglich von *dwStackSize* angegebene Größe, für die ein Commit ausgeführt wurde, jedoch größer oder gleich der Standardreservegröße ist, wird diese neue Commitgröße auf das nächste Vielfache von 1 MB aufgerundet.

Legen Sie zum Ändern der reservierten Stapelgröße den *parameter dwCreationFlags* von [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) oder [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) auf STACK \_ SIZE \_ PARAM IS A RESERVATION \_ \_ \_ fest, und verwenden Sie den parameter *dwStackSize.* In diesem Fall ist die Größe, für die ursprünglich ein Commit ausgeführt wurde, die Standardgröße, die im ausführbaren Header angegeben ist. Verwenden Sie für Fibers den *dwStackReserveSize-Parameter* von [**CreateFiberEx.**](/windows/desktop/api/WinBase/nf-winbase-createfiberex) Die Größe des Commits wird im *dwStackCommitSize-Parameter* angegeben.

Die [**SetThreadStackGuarantee-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) legt die mindeste Größe des Stapels fest, der dem aufrufenden Thread oder der aufrufenden Fiber zugeordnet ist, der während aller Stapelüberlauf-Ausnahmen verfügbar sein wird.

 

 
