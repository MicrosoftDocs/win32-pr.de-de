---
title: Netfile-Funktionen (Netzwerkverwaltung)
description: Die Funktionen der Netzwerk Verwaltungs Datei bieten eine Möglichkeit zum Überwachen und Schließen der Datei, des Geräts und der Pipe-Ressourcen, die auf einem Server geöffnet sind. Die Dateifunktionen sind nachfolgend aufgeführt.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517306"
---
# <a name="netfile-functions-network-management"></a>Netfile-Funktionen (Netzwerkverwaltung)

Die Funktionen der Netzwerk Verwaltungs Datei bieten eine Möglichkeit zum Überwachen und Schließen der Datei, des Geräts und der Pipe-Ressourcen, die auf einem Server geöffnet sind. Die Dateifunktionen sind nachfolgend aufgeführt.



| Funktion                                | BESCHREIBUNG                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**Netfileclose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Erzwingt das Schließen einer Ressource.                                          |
| [**Netfileaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Gibt Informationen zu geöffneten Dateien auf einem Server zurück.                    |
| [**Netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Gibt Informationen zu einem bestimmten Öffnen einer Server Ressource zurück. |



 

Wenn die Datei nicht auf andere Weise geschlossen werden kann, wird die [**netfileclose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) -Funktion aufgerufen. Diese Funktion sollte mit Vorsicht verwendet werden, da **netfileclose** keine Daten schreibt, die auf dem Client System zwischengespeichert wurden, bevor die Datei geschlossen wird.

Die [**netfileenum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) -Funktion gibt Informationen zu Ressourcen zurück, die auf einem Server geöffnet sind. Eine Datei kann von einer oder mehreren Anwendungen einmal oder mehrmals geöffnet werden. Alle Datei öffnenden werden eindeutig identifiziert. Die **netfileenum** -Funktion gibt einen Eintrag für jede Datei, die geöffnet wird, zurück. Die [**netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) -Funktion gibt Informationen zu einem Öffnen einer Ressource zurück.

Dateiinformationen sind auf folgenden Ebenen verfügbar:

-   [**Datei \_ Informationen \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [**Datei \_ Info \_ 3**](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

Die Ebenen 0 und 1 werden nicht unterstützt. Ebene 2 gibt nur die Identifikationsnummer zurück, die der Ressource zugewiesen wurde, als Sie geöffnet wurde. Auf Ebene 3 werden die Identifikationsnummer, Berechtigungen, Dateisperren und der Name des Benutzers, der die Ressource geöffnet hat, zurückgegeben.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen [**netfileenum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) und [**netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) erreichen können. Weitere Informationen finden Sie unter [**iadsresource**](/windows/desktop/api/iads/nn-iads-iadsresource) und [**iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
