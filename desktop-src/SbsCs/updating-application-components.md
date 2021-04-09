---
description: Parallele private Assemblys können verwendet werden, um Komponenten zu erstellen, die problemlos aktualisiert werden können, ohne auch die Hostinganwendung zu aktualisieren.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Anwendungskomponenten werden aktualisiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958846"
---
# <a name="updating-application-components"></a>Anwendungskomponenten werden aktualisiert

Parallele private Assemblys können verwendet werden, um Komponenten zu erstellen, die problemlos aktualisiert werden können, ohne auch die Hostinganwendung zu aktualisieren. Dies ermöglicht es einem aktualisierbaren Dienst, die aktualisierten Komponenten der Anwendung zu installieren, die Anwendung neu zu starten und die Anwendung die Änderungen zu verwenden. Wenn Anwendungs Manifeste verwendet werden, können die Funktionen von-Komponenten, die von einer Anwendung gehostet werden, aktualisiert werden, ohne dass der Code der Host Anwendung geändert werden muss.

Diese Methode kann verwendet werden, um die Version der Ressourcen einer Anwendung zu aktualisieren. Wenn eine Anwendung z. b. eine Assembly enthält, kann das Manifest der Anwendung eine Abhängigkeit von dieser Assembly angeben. Die Anwendung kann die Assembly abrufen, indem Sie [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) aufrufen, um die erforderlichen Dateien zu suchen und zu laden. Ein Updater muss einfach die neuesten Bits für die Assembly herunterladen, die nebeneinander mit einer früheren Version der Assembly vorhanden sein kann.

 

 
