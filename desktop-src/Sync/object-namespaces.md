---
description: Ein Objektnamespace schützt benannte Objekte vor nicht autorisiertem Zugriff.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Objektnamespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6137d53e45f27a8de2c76075bc2a5565a5942bd38bf6fa3cd3891e4561870b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765487"
---
# <a name="object-namespaces"></a>Objektnamespaces

Ein *Objektnamespace* schützt benannte Objekte vor nicht autorisiertem Zugriff. Durch das Erstellen eines privaten Namespace können Anwendungen und Dienste eine sicherere Umgebung erstellen.

Ein Prozess kann einen privaten Namespace mithilfe der [**CreatePrivateNamespace-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) erstellen. Diese Funktion erfordert, dass Sie eine Grenze *angeben,* die definiert, wie die Objekte im Namespace isoliert werden sollen. Der Aufrufer muss sich innerhalb der angegebenen Grenze befinden, damit der Erstellungsvorgang erfolgreich ist. Um eine Grenze anzugeben, verwenden Sie die [**Funktionen CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) und [**AddSIDToBoundaryDescriptor.**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor)

Der *lpAliasPrefix-Parameter* [**von CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) dient als Name des Namespace. Jeder Namespace wird durch seinen Namen und seine Grenzen eindeutig identifiziert. Das System unterstützt mehrere private Namespaces mit demselben Namen, solange sie unterschiedliche Grenzen angeben.

Angenommen, ein Prozess fordert die Erstellung eines Namespace NS1 an, der eine Grenze definiert, die zwei Elemente enthält: die Administrator-SID und die aktuelle Sitzungsnummer. Der Namespace wird erstellt, wenn der Prozess in der angegebenen Sitzung unter dem Administratorkonto ausgeführt wird. Ein anderer Prozess kann mithilfe der [**OpenPrivateNamespace-Funktion auf diesen Namespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) zugreifen. Sowohl der angegebene Name als auch die Grenze müssen übereinstimmen, wenn dieser Prozess den namespace öffnen soll, der vom ersten Prozess erstellt wurde. Beachten Sie, dass ein Prozess einen vorhandenen Namespace auch dann öffnen kann, wenn er sich nicht innerhalb der Grenze befindet, es sei denn, der Ersteller hat den Zugriff auf den Namespace mithilfe des *lpPrivateNamespaceAttributes-Parameters* eingeschränkt.

Die -Objekte, die in diesem Namespace erstellt werden, verfügen über Namen im Formular *Präfix* \\ *objektname*. Das Präfix ist der Namespacename, der durch den *lpAliasPrefix-Parameter* von [**CreatePrivateNamespace angegeben wird.**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) Um beispielsweise ein Ereignisobjekt namens MyEvent im NS1-Namespace zu erstellen, rufen Sie die [**CreateEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createeventa) auf, bei der *der lpName-Parameter* auf NS1 \\ MyEvent festgelegt ist.

Der Prozess, der den Namespace erstellt hat, kann die [**ClosePrivateNamespace-Funktion**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) verwenden, um das Handle für den Namespace zu schließen. Das Handle wird auch geschlossen, wenn der Prozess beendet wird, der den Namespace erstellt hat. Nachdem das Namespacehandle geschlossen wurde, tritt bei nachfolgenden Aufrufen von [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) ein Fehler auf, aber alle Vorgänge für Objekte im Namespace sind erfolgreich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernelobjektnamespaces](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
