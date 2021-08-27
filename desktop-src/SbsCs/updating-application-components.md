---
description: Mithilfe von gleichzeitigen privaten Assemblys können Komponenten erstellt werden, die problemlos aktualisiert werden können, ohne auch die Hostanwendung zu aktualisieren.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Aktualisieren von Anwendungskomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02948355143bc6f08c759ec6c2fe6009399cc6d8ca4b2bbd687e3d206c0e771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101590"
---
# <a name="updating-application-components"></a>Aktualisieren von Anwendungskomponenten

Mithilfe von gleichzeitigen privaten Assemblys können Komponenten erstellt werden, die problemlos aktualisiert werden können, ohne auch die Hostanwendung zu aktualisieren. Dadurch kann ein Aktualisierungsdienst die aktualisierten Komponenten der Anwendung installieren, die Anwendung neu starten und die Änderungen von der Anwendung verwenden lassen. Bei Verwendung von Anwendungsmanifesten kann die Funktionalität von Komponenten, die von einer Anwendung gehostet werden, aktualisiert werden, ohne den Code der Hostanwendung ändern zu müssen.

Diese Methode kann verwendet werden, um die Version der Ressourcen einer Anwendung zu aktualisieren. Wenn eine Anwendung beispielsweise eine Assembly enthält, kann das Manifest der Anwendung eine Abhängigkeit von dieser Assembly angeben. Die Anwendung kann die Assembly abrufen, indem [**sie SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) aufruft, um die benötigten Dateien zu suchen und zu laden. Ein Updater muss einfach die neuesten Bits für die Assembly herunterziehen, die nebeneinander mit einer früheren Version der Assembly vorhanden sein können.

 

 
