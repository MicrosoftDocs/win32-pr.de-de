---
description: Ein Objekt Namespace schützt benannte Objekte vor nicht autorisiertem Zugriff.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Objektnamespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3eed750bc91c128251cc66fd7f9ed167771150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865411"
---
# <a name="object-namespaces"></a>Objektnamespaces

Ein *Objekt Namespace* schützt benannte Objekte vor nicht autorisiertem Zugriff. Das Erstellen eines privaten Namespace ermöglicht Anwendungen und Diensten, eine sicherere Umgebung zu erstellen.

Ein Prozess kann einen privaten Namespace mithilfe der Funktion " [**kreateprivatenamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) " erstellen. Diese Funktion erfordert, dass Sie eine *Grenze* angeben, die definiert, wie die Objekte im Namespace isoliert werden sollen. Der Aufrufer muss sich innerhalb der angegebenen Grenze befinden, damit der Erstellungs Vorgang erfolgreich ausgeführt werden konnte. Um eine Grenze anzugeben, verwenden Sie die Funktionen [**"-Editor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) " und " [**addsidtoboundarydescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor) ".

Der *lpaliasprefix* -Parameter von " [**kreateprivatenamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) " dient als Name des Namespace. Jeder Namespace wird durch seinen Namen und seine Grenzen eindeutig identifiziert. Das System unterstützt mehrere private Namespaces mit demselben Namen, sofern Sie unterschiedliche Grenzen angeben.

Angenommen, ein Prozess fordert die Erstellung eines Namespace ns1 an, der eine Grenze definiert, die zwei Elemente enthält: die Administrator-SID und die aktuelle Sitzungsnummer. Der-Namespace wird erstellt, wenn der Prozess unter dem Administrator Konto in der angegebenen Sitzung ausgeführt wird. Ein anderer Prozess kann mit der [**openprivatenamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) -Funktion auf diesen Namespace zugreifen. Der angegebene Name und die angegebene Grenze müssen identisch sein, wenn dieser Prozess den vom ersten Prozess erstellten Namespace öffnen soll. Beachten Sie, dass ein Prozess einen vorhandenen Namespace auch dann öffnen kann, wenn er sich nicht innerhalb der Grenze befindet, es sei denn, der Ersteller hat den Zugriff auf den Namespace mithilfe des Parameters *lpprivatenamespaceattribute* eingeschränkt

Die Objekte, die in diesem Namespace erstellt werden, verfügen über Namen, die das Formular *prefix* \\ *objectName* aufweisen. Das Präfix ist der Namespace Name, der durch den *lpaliasprefix* -Parameter von " [**kreateprivatenamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea)" angegeben wird. Um z. b. ein Ereignis Objekt mit dem Namen "MyEvent" im ns1-Namespace zu erstellen, rufen Sie [**die Funktion "**](/windows/win32/api/synchapi/nf-synchapi-createeventa) -Funktion" auf, wobei der *lpname* -Parameter auf NS1 \\ MyEvent festgelegt ist

Der Prozess, der den-Namespace erstellt hat, kann die [**closeprivatenamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) -Funktion verwenden, um das Handle für den-Namespace zu schließen. Das Handle wird auch geschlossen, wenn der Prozess, der den Namespace erstellt hat, beendet wird. Nachdem das Namespace Handle geschlossen wurde, schlagen nachfolgende Aufrufe von [**openprivatenamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) fehl, aber alle Vorgänge für Objekte im-Namespace sind erfolgreich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernelobjektnamespaces](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
