---
title: Erstellen von Disketten mit mehreren Sitzungen
description: Mit IMAPI können Datenträger mit mehreren Sitzungen erstellt werden. Beim Erstellen einer mehr sitzenden CD müssen einige Punkte beachtet werden.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206599"
---
# <a name="creating-discs-with-multiple-sessions"></a>Erstellen von Disketten mit mehreren Sitzungen

Mit IMAPI können Datenträger mit mehreren Sitzungen erstellt werden. Beim Erstellen einer mehr sitzenden CD müssen einige Punkte beachtet werden.

Mit der [**idiscmaster:: setactivediscrecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) -Methode wird festgelegt, ob nach der Einstellung eine IMAPI-DVD mit mehreren Sitzungen auf dem aktiven Laufwerk vorhanden ist. Wenn dies der Fall ist, wechselt IMAPI automatisch in den multisitzungsmodus. Die Verwendung von [**clearformatcontent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) , nachdem der Modus für mehrere Sitzungen festgelegt wurde, bewirkt, dass IMAPI in den Einzel Sitzungs Modus wechselt. Dies bedeutet, dass für einen Datensatz mit [**recorddisk**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) ein leeres Laufwerk erforderlich ist. Wenn sich die Festplatte im Modus für mehrere Sitzungen befindet, muss sich die gleiche Festplatte im aktiven Recorder befinden, oder es wird ein Fehlercode von IMAPI \_ E \_ fehlerdisk zurückgegeben.

Die Auswahl einer Aufzeichnung im Joliet-Format bewirkt, dass IMAPI Informationen von der aktuell installierten CD liest. Wenn es sich bei der Festplatte um eine vorherige IMAPI-Joliet-CD handelt, die Platz für eine andere Sitzung hat, legt IMAPI automatisch den Modus für mehrere Sitzungen fest. Diese CD muss beim Aufruf von [**recorddisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc)in der aktiven Aufzeichnung vorhanden sein.

Das Schließen der ersten Sitzung auf einer CD erfordert 21 MB. Jede zusätzliche Sitzung benötigt 11 MB, um zu schließen.

 

 




