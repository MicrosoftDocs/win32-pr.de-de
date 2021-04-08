---
description: Bevor Sie ein Datei Protokoll verwenden können, müssen Sie setupinitializefilelog aufrufen, um es zu öffnen oder zu erstellen. Wenn Sie diese Funktion aufgerufen haben, können Sie Flags angeben, um ein Datei Protokoll zu erstellen oder zu überschreiben, das System Protokoll zu öffnen oder ein Datei Protokoll als schreibgeschützt zu öffnen.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Verwenden des Datei Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960998"
---
# <a name="using-the-file-log"></a>Verwenden des Datei Protokolls

Bevor Sie ein Datei Protokoll verwenden können, müssen Sie [**setupinitializefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) aufrufen, um es zu öffnen oder zu erstellen. Wenn Sie diese Funktion aufgerufen haben, können Sie Flags angeben, um ein Datei Protokoll zu erstellen oder zu überschreiben, das System Protokoll zu öffnen oder ein Datei Protokoll als schreibgeschützt zu öffnen.

Nachdem [**setupinitializefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) ein Handle für ein Datei Protokoll zurückgegeben hat, können Sie einen Eintrag hinzufügen, indem Sie [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)aufrufen, einen Eintrag durch Aufrufen von [**setupremumuvefilelogentry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)löschen oder Informationen zu einer bestimmten Datei in einem Datei Protokoll abrufen, indem Sie [**setupqueryfilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)aufrufen.

Wenn das Datei Protokoll nicht mehr benötigt wird, sollte [**setupterminatefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) aufgerufen werden, um die während des Aufrufs von [**setupinitializefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)zugeordneten Ressourcen freizugeben.

 

 



