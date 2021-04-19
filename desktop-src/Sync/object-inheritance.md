---
description: Wenn Sie einen Prozess mit der Funktion "-Funktion" erstellen, können Sie angeben, dass der Prozess Handles für Mutex, Ereignis, Semaphore oder Zeit Geber Objekte mithilfe der Struktur der Sicherheits Attribute erbt \_ .
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Objektvererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349522"
---
# <a name="object-inheritance"></a>Objektvererbung

Wenn Sie einen Prozess mit [**der Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) -Funktion" erstellen, können Sie angeben, dass der Prozess Handles für Mutex, Ereignis, Semaphore oder Zeit Geber Objekte mithilfe der Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) erbt. Das vom Prozess geerbte handle hat denselben Zugriff auf das Objekt wie das ursprüngliche handle. Der geerbte Handle wird in der Handle-Tabelle des erstellten Prozesses angezeigt, aber Sie müssen den Handle-Wert an den erstellten Prozess übermitteln. Dies können Sie erreichen, indem Sie den Wert als Befehlszeilenargument angeben, wenn Sie "up **Process Process**" aufrufen. Der erstellte Prozess verwendet dann die [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) -Funktion, um die Befehlszeilen Zeichenfolge abzurufen, und konvertiert das Handle-Argument in ein verwendbares handle. Weitere Informationen finden Sie unter [Vererbung](../procthread/inheritance.md).

 

 
