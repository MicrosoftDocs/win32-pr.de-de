---
description: Die Verbinden-Methode des Mergeobjekts kann verwendet werden, um ein Modul mit einem zusätzlichen Feature zu verbinden, das mit der Datenbank zusammengeführt wurde oder mit der Datenbank zusammengeführt wird. Das Feature muss vorhanden sein, bevor diese Methode aufgerufen wird.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Verbinden eines Mergemoduls mit mehreren Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12044ff293d825c160533907d625a2d12bb9ea217233c54dd9d5a0099990ee3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948421"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Verbinden eines Mergemoduls mit mehreren Features

Die [**Verbinden-Methode**](merge-connect.md) des [Mergeobjekts](merge-object.md) kann verwendet werden, um ein Modul mit einem zusätzlichen Feature zu verbinden, das mit der Datenbank zusammengeführt wurde oder mit der Datenbank zusammengeführt wird. Das Feature muss vorhanden sein, bevor diese Methode aufgerufen wird.

Ein Mergemodul sollte niemals eine Komponente mit Systemdateien an das Hauptfeature einer Anwendung übermitteln, da dies dazu führen kann, dass der Installer die Anwendung bei jeder Verwendung der Systemdatei überprüft und repariert. Eine .msi Datei, die Komponenten aus einem Mergemodul akzeptieren soll, sollte so erstellt werden, dass alle Komponenten, die Systemdateien enthalten, nur zu Features gehören, die vom Hauptfeature der Anwendung getrennt sind.

Wenn Ihr Paket ein Mergemodul mit Systemdateien verwendet, die alle Komponenten aus dem Mergemodul mit dem Hauptfeature der Anwendung verknüpfen, kann ein Versuch, die Systemdatei zu verwenden, dazu führen, dass der Installer versucht, das Hauptfeature der Anwendung zu reparieren. Wenn das Hauptfeature nicht repariert werden kann, schlägt die Installation möglicherweise fehl.

 

 



