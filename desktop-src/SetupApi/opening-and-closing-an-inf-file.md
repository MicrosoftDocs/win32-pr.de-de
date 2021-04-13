---
description: Bevor die Setup Funktionen auf Informationen in der INF zugreifen können, müssen Sie Sie mit einem Aufrufen der setupopeninffile-Funktion öffnen. Diese Funktion gibt ein Handle für die INF-Datei zurück.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Öffnen und Schließen einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529324"
---
# <a name="opening-and-closing-an-inf-file"></a>Öffnen und Schließen einer INF-Datei

Bevor die Setup Funktionen auf Informationen in der INF zugreifen können, müssen Sie Sie mit einem Aufrufen der [**setupopeninffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) -Funktion öffnen. Diese Funktion gibt ein Handle für die INF-Datei zurück.

Wenn Sie den Namen der INF-Datei, die Sie öffnen müssen, nicht kennen, können Sie die [**setupgetinffilelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) -Funktion verwenden, um eine Liste der INF-Dateien in einem Verzeichnis abzurufen.

Nachdem Sie eine INF-Datei geöffnet haben, können Sie zusätzliche INF-Dateien an die geöffnete INF-Datei anfügen, indem Sie die [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) -Funktion verwenden. Dies ist funktionell vergleichbar mit einer include-Anweisung. Wenn nachfolgende Setup Funktionen auf eine geöffnete INF-Datei verweisen, können Sie auch auf alle in den angefügten Dateien gespeicherten Informationen zugreifen.

Wenn Sie beim Aufrufen der [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) -Funktion keine INF-Datei angeben, fügt **setupopenappendinffile** die Dateien, die vom **Layoutfile** -Schlüssel angegeben werden, im Abschnitt **Version** der geöffneten INF-Datei an.

Wenn Sie die Informationen in der INF-Datei nicht mehr benötigen, rufen Sie die [**setupcloseinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) -Funktion auf, um die während des Aufrufes [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)zugeordneten Ressourcen freizugeben.

 

 



