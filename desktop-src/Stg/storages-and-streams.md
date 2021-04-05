---
title: Storages und Streams
description: Ein Speicher Objekt ist analog zu einem Dateisystem Verzeichnis.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708352"
---
# <a name="storages-and-streams"></a>Storages und Streams

Ein Speicher Objekt ist analog zu einem Dateisystem Verzeichnis. Ebenso wie ein Verzeichnis andere Verzeichnisse und Dateien enthalten kann, kann ein Speicher Objekt andere Speicher Objekte und Streamobjekte enthalten. Ebenso wie ein Verzeichnis verfolgt ein Speicher Objekt die Speicherorte und Größen der untergeordneten Speicher Objekte und Streamobjekte.

Ein Stream-Objekt entspricht dem herkömmlichen Konzept einer Datei. Wie eine-Datei enthält ein Stream Daten, die als aufeinander folgende Byte Sequenz gespeichert werden.

Eine com-Verbund Datei besteht aus einem Stamm Speicher Objekt, das mindestens ein Stream-Objekt enthält, das die systemeigenen Daten zusammen mit einem oder mehreren Speicher Objekten darstellt, die den verknüpften und eingebetteten Objekten entsprechen. Das Stamm Speicher Objekt ist einem Dateinamen in dem Dateisystem zugeordnet, in dem es sich befindet. Jedes der Objekte innerhalb des Dokuments wird auch durch ein Speicher Objekt dargestellt, das mindestens ein Streamobjekt enthält, das möglicherweise auch ein oder mehrere Speicher Objekte enthält. Auf diese Weise kann ein Dokument aus einer unbegrenzten Anzahl von in der Liste unter fallenen Objekten bestehen. Weitere Informationen finden Sie unter [Verbund Dateien](compound-files.md).

 

 




