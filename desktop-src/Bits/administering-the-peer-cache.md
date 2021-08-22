---
title: Verwalten des Peercaches
description: Hinweis Ab Windows 7 ist das Peercachingmodell Background Intelligent Transfer Service (BITS) 3.0 veraltet.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3821cc0894754b8dbc2ee9f9a189381ac69030d39938c8f6cb4bc52625ef03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588750"
---
# <a name="administering-the-peer-cache"></a>Verwalten des Peercaches

> [!Note]  
> Ab Windows 7 ist das Peercachingmodell Background Intelligent Transfer Service (BITS) 3.0 veraltet. Wenn BITS 4.0 installiert ist, ist das PEERcachingmodell von BITS 3.0 nicht verfügbar.

 

Zur Verbesserung der Downloadleistung können Sie mit BITS Inhalte von Peercomputern herunterladen. Um dieses Feature zu aktivieren, muss der Administrator die Gruppenrichtlinieneinstellung EnablePeerCaching aktivieren. Wenn diese Option aktiviert ist, kann der Peer Inhalte von Peers herunterladen und Inhalte für Peers zur Verfügung haben. Der Administrator kann auch die Richtlinieneinstellungen DisablePeerCachingClient und DisablePeerCachingServer verwenden, um zu verhindern, dass Inhalte von einem Peer heruntergeladen oder Inhalte an Peers übergeben werden.

Wenn die Gruppenrichtlinieneinstellungen nicht konfiguriert sind, kann eine Anwendung die [**IBitsPeerCacheAdministration::SetConfigurationFlags-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) aufrufen, um die Peercachingpräferenz für den Computer festlegen. Beachten Sie, dass diese Einstellungen durch die Gruppenrichtlinieneinstellungen überschrieben werden, wenn sie später festgelegt werden. Um zu ermitteln, ob der Computer peer caching aktiviert, rufen Sie die [**IBitsPeerCacheAdministration::GetConfigurationFlags-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) auf.

Wenn die Peerzwischenspeicherung aktiviert ist, speichert BITS den Inhalt eines Auftrags nur zwischen, wenn der Inhalt des Auftrags explizit zwischengespeichert werden kann. BITS wird inhalte auch nur von einem Peer herunterladen, wenn der Auftrag dies explizit zulässt. Um die Peerzwischenspeicherung für einen Auftrag zu aktivieren, rufen Sie die [**IBackgroundCopyJob4::SetPeerCachingFlags-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) auf.

Zusätzlich zur Verwendung von Gruppenrichtlinie oder der [**IBitsPeerCacheAdministration-Schnittstelle**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) zum Aktivieren der Peerzwischenspeicherung können Sie auch eine der beiden Methoden verwenden, um die Standardcachegröße und -dauer zu ändern, die eine Datei, auf die nicht zugegriffen wird, im Cache verbleibt. Um die Standardwerte mithilfe der **IBitsPeerCacheAdministration-Schnittstelle** zu ändern, rufen Sie die [**Methoden SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) und [**SetMaximumContentAge**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) auf. Da diese Methoden die Einstellungseinstellungen festlegen, werden sie von den Gruppenrichtlinieneinstellungen überschrieben.

Um die Peers auflisten zu können, von denen BITS versucht, Inhalte herunterzuladen, rufen Sie die [**IBitsPeerCacheAdministration::EnumPeers-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) auf.

Rufen Sie die [**IBitsPeerCacheAdministration::EnumRecords-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) auf, um die Dateien im Cache auflisten zu können, die BITS für Peers verwendet.

Sie sollten den Peercache niemals verwalten müssen, um Peers zu finden oder Cachedatensätze zu löschen. Diese Funktionalität wurde der Vollständigkeit halber in der [**IBitsPeerCacheAdministration-Schnittstelle**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) enthalten.

 

 




