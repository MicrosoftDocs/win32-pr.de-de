---
description: Bevor die Setupfunktionen auf Informationen in der INF zugreifen können, müssen Sie sie mit einem Aufruf der SetupOpenInfFile-Funktion öffnen. Diese Funktion gibt ein Handle für die INF-Datei zurück.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Öffnen und Schließen einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05500b473a904a3834fa507cff0d22c466153f4e08d95f75d0c076c66d86675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665550"
---
# <a name="opening-and-closing-an-inf-file"></a>Öffnen und Schließen einer INF-Datei

Bevor die Setupfunktionen auf Informationen in der INF zugreifen können, müssen Sie sie mit einem Aufruf der [**SetupOpenInfFile-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) öffnen. Diese Funktion gibt ein Handle für die INF-Datei zurück.

Wenn Sie den Namen der INF-Datei nicht kennen, die Sie öffnen müssen, können Sie die [**SetupGetInfFileList-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) verwenden, um eine Liste der INF-Dateien in einem Verzeichnis abzurufen.

Nachdem Sie eine INF-Datei geöffnet haben, können Sie mithilfe der Funktion [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) zusätzliche INF-Dateien an die geöffnete INF-Datei anfügen. Dies ähnelt funktional einer include-Anweisung. Wenn nachfolgende Setupfunktionen auf eine geöffnete INF-Datei verweisen, können sie auch auf alle Informationen zugreifen, die in den angefügten Dateien gespeichert sind.

Wenn Sie während des Aufrufs der [**SetupOpenAppendInfFile-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) keine INF-Datei angeben, fügt **SetupOpenAppendInfFile** die durch den **LayoutFile-Schlüssel** im Abschnitt **Version** der geöffneten INF-Datei angegebenen Dateien an.

Wenn Sie die Informationen in der INF-Datei nicht mehr benötigen, rufen Sie die [**SetupCloseInfFile-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) auf, um Ressourcen freizugeben, die während des Aufrufs von [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)zugeordnet wurden.

 

 



