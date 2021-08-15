---
description: Die Netzwerkdateifunktionen bieten eine Möglichkeit, die auf einem Server geöffneten Datei-, Geräte- und Piperessourcen zu überwachen und zu schließen. Die Dateifunktionen sind im Folgenden aufgeführt.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: NetFile-Funktionen (Netzwerkfreigabeverwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efdd1a9339701ccbb534a91b9dfe0423bea546e8d474455c2a6ffdda02adab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362611"
---
# <a name="netfile-functions-network-share-management"></a>NetFile-Funktionen (Netzwerkfreigabeverwaltung)

Die Netzwerkdateifunktionen bieten eine Möglichkeit, die auf einem Server geöffneten Datei-, Geräte- und Piperessourcen zu überwachen und zu schließen. Die Dateifunktionen sind im Folgenden aufgeführt.



| Funktion                                 | BESCHREIBUNG                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Erzwingt das Schließen einer Ressource.                                          |
| [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Gibt Informationen zu geöffneten Dateien auf einem Server zurück.                    |
| [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Gibt Informationen zu einem bestimmten Öffnen einer Serverressource zurück. |



 

Rufen Sie die [**NetFileClose-Funktion**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) auf, wenn die Datei nicht auf andere Weise geschlossen werden kann. Diese Funktion sollte mit Vorsicht verwendet werden, da **NetFileClose** keine auf dem Clientsystem zwischengespeicherten Daten in die Datei schreibt, bevor die Datei geschlossen wird.

Die [**NetFileEnum-Funktion**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) gibt Informationen zu Ressourcen zurück, die auf einem Server geöffnet sind. Eine Datei kann von einer oder mehreren Anwendungen ein oder mehrere Male geöffnet werden. Jede Datei, die geöffnet wird, wird eindeutig identifiziert. Die **NetFileEnum-Funktion** gibt einen Eintrag für jedes Öffnen der Datei zurück. Die [**NetFileGetInfo-Funktion**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) gibt Informationen zum Öffnen einer Ressource zurück.

Dateiinformationen sind auf den folgenden Ebenen verfügbar.

<dl>

[**DATEIINFORMATIONEN \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**DATEIINFORMATIONEN \_ \_ 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

Die Ebenen 0 und 1 werden nicht unterstützt. Ebene 2 gibt nur die ID zurück, die der Ressource beim Öffnen zugewiesen wurde. Ebene 3 gibt die ID, berechtigungen, Dateisperren und den Namen des Benutzers zurück, der die Ressource geöffnet hat.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der [**Funktionen NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) und [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) erreichen können. Weitere Informationen finden Sie unter [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) und [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)

 

 
