---
description: Die Netzwerkdatei Funktionen bieten eine Möglichkeit zum Überwachen und Schließen der Datei, des Geräts und der Pipe-Ressourcen, die auf einem Server geöffnet sind. Die Dateifunktionen sind nachfolgend aufgeführt.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Netfile-Funktionen (Netzwerkfreigabe Verwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363337"
---
# <a name="netfile-functions-network-share-management"></a>Netfile-Funktionen (Netzwerkfreigabe Verwaltung)

Die Netzwerkdatei Funktionen bieten eine Möglichkeit zum Überwachen und Schließen der Datei, des Geräts und der Pipe-Ressourcen, die auf einem Server geöffnet sind. Die Dateifunktionen sind nachfolgend aufgeführt.



| Funktion                                 | BESCHREIBUNG                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**Netfileclose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Erzwingt das Schließen einer Ressource.                                          |
| [**Netfileaufumum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Gibt Informationen zu geöffneten Dateien auf einem Server zurück.                    |
| [**Netfilegetinfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Gibt Informationen zu einem bestimmten Öffnen einer Server Ressource zurück. |



 

Wenn die Datei nicht auf andere Weise geschlossen werden kann, wird die [**netfileclose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) -Funktion aufgerufen. Diese Funktion sollte mit Vorsicht verwendet werden, da **netfileclose** keine Daten schreibt, die auf dem Client System zwischengespeichert wurden, bevor die Datei geschlossen wird.

Die [**netfileenum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) -Funktion gibt Informationen zu Ressourcen zurück, die auf einem Server geöffnet sind. Eine Datei kann von einer oder mehreren Anwendungen einmal oder mehrmals geöffnet werden. Alle Datei öffnenden werden eindeutig identifiziert. Die **netfileenum** -Funktion gibt einen Eintrag für jede Datei, die geöffnet wird, zurück. Die [**netfilegetinfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) -Funktion gibt Informationen zu einem Öffnen einer Ressource zurück.

Dateiinformationen sind auf den folgenden Ebenen verfügbar.

<dl>

[**Datei \_ Informationen \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**Datei \_ Info \_ 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

Die Ebenen 0 und 1 werden nicht unterstützt. Ebene 2 gibt nur die Identifikationsnummer zurück, die der Ressource zugewiesen wurde, als Sie geöffnet wurde. Auf Ebene 3 werden die Identifikationsnummer, Berechtigungen, Dateisperren und der Name des Benutzers, der die Ressource geöffnet hat, zurückgegeben.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen [**netfileenum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) und [**netfilegetinfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) erreichen können. Weitere Informationen finden Sie unter [**iadsresource**](/windows/desktop/api/iads/nn-iads-iadsresource) und [**iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
