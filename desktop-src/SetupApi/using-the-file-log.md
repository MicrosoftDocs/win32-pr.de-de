---
description: Bevor Sie ein Dateiprotokoll verwenden können, müssen Sie SetupInitializeFileLog aufrufen, um es zu öffnen oder zu erstellen. Wenn Sie diese Funktion aufrufen, können Sie Flags angeben, um ein Dateiprotokoll zu erstellen oder zu überschreiben, das Systemprotokoll zu öffnen oder ein Dateiprotokoll als schreibgeschützt zu öffnen.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Verwenden des Dateiprotokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39772a668f3e0920df6f7f023ed481de5f9676954b276625335772220eab385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117963908"
---
# <a name="using-the-file-log"></a>Verwenden des Dateiprotokolls

Bevor Sie ein Dateiprotokoll verwenden können, müssen Sie [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) aufrufen, um es zu öffnen oder zu erstellen. Wenn Sie diese Funktion aufrufen, können Sie Flags angeben, um ein Dateiprotokoll zu erstellen oder zu überschreiben, das Systemprotokoll zu öffnen oder ein Dateiprotokoll als schreibgeschützt zu öffnen.

Nachdem [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) einem Dateiprotokoll ein Handle zurückgegeben hat, können Sie einen Eintrag hinzufügen, indem Sie [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)aufrufen, einen Eintrag löschen, indem Sie [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)aufrufen oder Informationen zu einer bestimmten Datei in einem Dateiprotokoll abrufen, indem [**Sie SetupQueryFileLog aufrufen.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)

Wenn das Dateiprotokoll nicht mehr benötigt wird, sollte [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) aufgerufen werden, um die Während des Aufrufs von [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)zugeordneten Ressourcen frei zu geben.

 

 



