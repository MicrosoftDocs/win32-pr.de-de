---
description: Die Connect-Methode des Merge-Objekts kann verwendet werden, um ein Modul mit einer zusätzlichen Funktion zu verbinden, die in der Datenbank zusammengeführt oder in der Datenbank zusammengeführt wird. Die Funktion muss vorhanden sein, bevor diese Methode aufgerufen wird.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Verbinden eines Mergemoduls mit mehreren Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867044"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Verbinden eines Mergemoduls mit mehreren Features

Die [**Connect**](merge-connect.md) -Methode des [Merge-Objekts](merge-object.md) kann verwendet werden, um ein Modul mit einer zusätzlichen Funktion zu verbinden, die in der Datenbank zusammengeführt oder in der Datenbank zusammengeführt wird. Die Funktion muss vorhanden sein, bevor diese Methode aufgerufen wird.

Ein Mergemodul sollte nie eine Komponente, die Systemdateien enthält, an das Haupt Feature einer Anwendung übermitteln, da dies dazu führen kann, dass das Installationsprogramm die Anwendung bei jeder Verwendung der Systemdatei überprüft und repariert. Eine MSI-Datei, die Komponenten eines Mergemoduls akzeptieren soll, sollte so erstellt werden, dass alle Komponenten, die Systemdateien enthalten, nur zu Features gehören, die von der Hauptfunktion der Anwendung getrennt sind.

Wenn das Paket ein Mergemodul verwendet, das Systemdateien enthält, die alle Komponenten aus dem Mergemodul mit dem Haupt Feature der Anwendung verknüpfen, kann der Versuch, die Systemdatei zu verwenden, das Installationsprogramm veranlassen, das Haupt Feature der Anwendung zu reparieren. Wenn die Hauptfunktion nicht repariert werden kann, tritt bei der Installation möglicherweise ein Fehler auf.

 

 



