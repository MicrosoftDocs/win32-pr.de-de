---
description: Zeitstempel sind normalerweise enthalten, wenn eine Datei mit SignTool mit der Option -t signiert wird.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Hinzufügen von Zeitstempeln zu zuvor signierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880230"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Hinzufügen von Zeitstempeln zu zuvor signierten Dateien

Zeitstempel sind normalerweise enthalten, wenn eine Datei mit SignTool mit der Option **-t** signiert wird. Außerdem können Zeitstempel zu Dateien hinzugefügt werden, die ohne Zeitstempel signiert wurden. Der folgende Befehl fügt einer zuvor signierten Datei einen Zeitstempel hinzu:

**signtool timestamp -t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> Die Datei, die mit einem Zeitstempel versehen werden soll, muss zuvor signiert worden sein.

 

Weitere Informationen zu SignTool finden Sie unter [SignTool](signtool.md).

 

 



