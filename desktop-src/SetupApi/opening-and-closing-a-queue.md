---
description: Bevor Sie Datei Vorgänge in die Warteschlange stellen können, müssen Sie eine Datei Warteschlange öffnen. Durch Aufrufen der setupopenfilequeue-Funktion wird ein Handle für eine Warteschlangen Datei zurückgegeben. Dieses Handle wird von nachfolgenden Warteschlangen Funktionen verwendet, um auf die geöffnete Warteschlange zu verweisen und Vorgänge hinzuzufügen oder Sie zu scannen.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Öffnen und Schließen einer Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357922"
---
# <a name="opening-and-closing-a-queue"></a>Öffnen und Schließen einer Warteschlange

Bevor Sie Datei Vorgänge in die Warteschlange stellen können, müssen Sie eine Datei Warteschlange öffnen. Durch Aufrufen der [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) -Funktion wird ein Handle für eine Warteschlangen Datei zurückgegeben. Dieses Handle wird von nachfolgenden Warteschlangen Funktionen verwendet, um auf die geöffnete Warteschlange zu verweisen und Vorgänge hinzuzufügen oder Sie zu scannen.

Nachdem alle angegebenen Datei Vorgänge in die Warteschlange eingereiht und ein Commit ausgeführt wurden, müssen Sie die Funktion [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) aufrufen, um beim Aufrufen von [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)zugeordnete Ressourcen freizugeben.

> [!Note]  
> Die Funktion " [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) " führt keinen Commit für die Datei Warteschlange aus. Alle Vorgänge, für die ein Commit ausgeführt wird, wenn **setupclosefilequeue** aufgerufen wird, werden nicht ausgeführt.

 

 

 



