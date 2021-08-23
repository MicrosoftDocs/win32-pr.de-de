---
description: Wenn Sie einen Prozess mit der CreateProcess-Funktion erstellen, können Sie angeben, dass der Prozess Handles an Mutex-, Ereignis-, Semaphor- oder Timerobjekte erbt, indem Sie die \_ SECURITY ATTRIBUTES-Struktur verwenden.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Objektvererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661380"
---
# <a name="object-inheritance"></a>Objektvererbung

Wenn Sie einen Prozess mit der [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) erstellen, können Sie angeben, dass der Prozess Handles an Mutex-, Ereignis-, Semaphor- oder Timerobjekte erbt, indem Sie die [**SECURITY \_ ATTRIBUTES-Struktur**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) verwenden. Das vom Prozess geerbte Handle hat den gleichen Zugriff auf das Objekt wie das ursprüngliche Handle. Das geerbte Handle wird in der Handletabelle des erstellten Prozesses angezeigt, Aber Sie müssen den Handlewert dem erstellten Prozess mitteilen. Sie können dies erreichen, indem Sie den Wert als Befehlszeilenargument angeben, wenn Sie **CreateProcess** aufrufen. Der erstellte Prozess verwendet dann die [**GetCommandLine-Funktion,**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) um die Befehlszeilenzeichenfolge abzurufen und das Handleargument in ein verwendbares Handle zu konvertieren. Weitere Informationen finden Sie unter [Vererbung](../procthread/inheritance.md).

 

 
