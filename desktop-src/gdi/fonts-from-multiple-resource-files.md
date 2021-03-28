---
description: Schriftarten aus mehreren Ressourcen Dateien
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Schriftarten aus mehreren Ressourcen Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2021
ms.locfileid: "104996450"
---
# <a name="fonts-from-multiple-resource-files"></a>Schriftarten aus mehreren Ressourcen Dateien

In der Regel ist eine Schriftart in einer einzelnen Schriftart Ressourcen Datei enthalten. Die Informationen für einige Schriftarten sind jedoch auf mehrere Dateien verteilt. Beispielsweise sind für Typ 1 mehrere Master Schriftarten zwei Dateien erforderlich:

-   PFM für die Schriftart Metrik
-   PFB für Schriftart Bits

Um dem System eine Schriftart aus mehreren Dateien hinzuzufügen, verwenden Sie die Funktionen [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) oder [**addfontresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) . Der *lpszfilename* -Parameter in diesen Funktionen muss auf eine Zeichenfolge verweisen, die die Dateinamen enthält, die durch einen senkrechten Strich oder eine Pipe () getrennt sind \| . Um z. b. abcxxxxx. PFM und abcxxxxx. PFB für eine Schriftart vom Typ 1 anzugeben, verwenden Sie die Zeichenfolge "abcxxxxx. PFM \| abcxxxxx. PFB".

[**Addfontresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) unterscheidet sich von [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) dahin, dass die Anwendung, die **addfontresourceex** aufruft, die Schriftart als privat oder nicht Aufzähl Bar angeben kann.

Um eine Schriftart aus einem Speicher Image hinzuzufügen, verwenden Sie [**addfontmemresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex). Dadurch kann eine Anwendung eine Schriftart verwenden, die in ein Dokument oder eine Webseite eingebettet ist.

Um eine Schriftart zu entfernen, die aus mehreren Ressourcen Dateien stammt, müssen Sie [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) oder [**removefontresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)aufrufen, je nachdem, welche Funktion zum Hinzufügen der Schriftart verwendet wurde. Sie müssen die gleichen Flags angeben, die zum Hinzufügen der Schriftart verwendet wurden. Verwenden Sie [**removefontmemresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex), um eine Schriftart zu entfernen, die aus einem Speicher Abbild hinzugefügt wurde.

Die Verwendung einer Schriftart, die aus mehreren Schriftart Ressourcen Dateien stammt, ist identisch mit der Verwendung einer Schriftart aus einer einzelnen Ressourcen Datei.

 

 
