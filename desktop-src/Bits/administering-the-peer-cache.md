---
title: Verwalten des Peer Caches
description: Hinweis ab Windows 7 ist das Peer Caching-Modell Background Intelligent Transfer Service (Bits) 3,0 als veraltet markiert.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b3ea1dd19c9aca855ffd73e174dcb3b588a54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708375"
---
# <a name="administering-the-peer-cache"></a>Verwalten des Peer Caches

> [!Note]  
> Ab Windows 7 ist das Peer Caching-Modell Background Intelligent Transfer Service (Bits) 3,0 veraltet. Wenn BITS 4,0 installiert ist, ist das Peer Cache Modell Bits 3,0 nicht verfügbar.

 

Um die Download Leistung zu verbessern, können Sie mit Bits Inhalt von Peer Computern herunterladen. Um dieses Feature zu aktivieren, muss der Administrator die Gruppenrichtlinien Einstellung enablepeer Caching aktivieren. Wenn diese Option aktiviert ist, kann der Peer Inhalte von Peers herunterladen und Inhalte für Peers bereitstellen. Der Administrator kann auch die Richtlinien Einstellungen disablepeercachingclient und disablepeercachingserver verwenden, um das Herunterladen von Inhalten von einem Peer oder das bereitzustellen von Inhalten an Peers zu verhindern.

Wenn die Gruppenrichtlinien Einstellungen nicht konfiguriert sind, kann eine Anwendung die [**ibitspeercacheadministration:: setconfigurationflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) -Methode aufrufen, um die Peer Caching-Einstellung für den Computer festzulegen. Beachten Sie, dass diese Einstellungen durch die Gruppenrichtlinien Einstellungen überschrieben werden, wenn Sie später festgelegt werden. Um zu ermitteln, ob der Computer Peer Caching aktiviert, müssen Sie die [**ibitspeercacheadministration:: getconfigurationflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) -Methode aufrufen.

Wenn die Peer Zwischenspeicherung aktiviert ist, speichert Bits nur den Inhalt eines Auftrags zwischen, wenn der Auftrag explizit zulässt, dass der Inhalt zwischengespeichert wird. Bits lädt auch Inhalt von einem Peer nur herunter, wenn der Auftrag dies explizit zulässt. Um Peer Caching für einen Auftrag zu aktivieren, müssen Sie die [**IBackgroundCopyJob4:: setpeercachingflags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) -Methode aufrufen.

Zusätzlich zur Verwendung von Gruppenrichtlinie oder der [**ibitspeercacheadministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) -Schnittstelle zum Aktivieren der Peer Zwischenspeicherung können Sie auch beide Methoden verwenden, um die Standard Cache Größe und die Zeitspanne zu ändern, für die eine Datei, auf die nicht zugegriffen wird, im Cache verbleibt. Um die Standardeinstellungen mithilfe der **ibitspeercacheadministration** -Schnittstelle zu ändern, müssen Sie die Methoden [**setmaximumcachesize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) und [**setmaximumcontentage**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) aufrufen. Da diese Methoden die Einstellungs Einstellungen festlegen, werden Sie durch die Gruppenrichtlinien Einstellungen überschrieben.

Um die Peers aufzulisten, von denen Bits versuchen, Inhalte herunterzuladen, nennen Sie die [**ibitspeercacheadministration:: enumpeers**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) -Methode.

Um die Dateien im Cache aufzulisten, die Bits für Peers bereitstellt, müssen Sie die [**ibitspeercacheadministration:: enumrecords**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) -Methode aufrufen.

Sie sollten den Peercache niemals in Bezug auf das Ermitteln von Peers oder das Löschen von Cache Datensätzen verwalten müssen. Diese Funktionalität war aus Gründen der Vollständigkeit in der Schnittstelle [**ibitspeercacheadministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) enthalten.

 

 




