---
title: Registrieren von com-Servern
description: Registrieren von com-Servern
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102378"
---
# <a name="registering-com-servers"></a>Registrieren von com-Servern

Nachdem Sie eine Klasse im Code definiert (um sicherzustellen, dass Sie [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) oder [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)implementiert) und ihr eine CLSID zugewiesen haben, müssen Sie Informationen in die Registrierung einfügen, die com bei Anforderung eines Clients mit der CLSID ermöglicht, Instanzen der zugehörigen Objekte zu erstellen. Diese Informationen informieren das System für eine bestimmte CLSID, in der sich der DLL-oder exe-Code für diese Klasse befindet und wie Sie gestartet werden soll.

Es gibt mehr als eine Möglichkeit, eine Klasse in der Registrierung zu registrieren. Außerdem gibt es andere Möglichkeiten, eine Klasse beim System zu registrieren, wenn Sie ausgeführt wird, damit das System weiß, dass sich ein aktuell laufendes Objekt im System befindet.

Weitere Informationen zum Registrieren von finden Sie in den folgenden Themen:

-   [Registrieren einer Klasse bei der Installation](registering-a-class-at-installation.md)
-   [Registrieren eines ausführenden exe-Servers](registering-a-running-exe-server.md)
-   [Registrieren von Objekten in der rot](registering-objects-in-the-rot.md)
-   [Selbstregistrierung](self-registration.md)
-   [Installieren von als Dienst Anwendung](installing-as-a-service-application.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuständigkeiten von com-Servern](com-server-responsibilities.md)
</dt> </dl>

 

 