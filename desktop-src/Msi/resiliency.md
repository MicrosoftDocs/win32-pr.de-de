---
description: Resilienz ist die Fähigkeit einer Anwendung, ordnungsgemäß aus Situationen wiederherzustellen, in denen eine wichtige Komponente fehlt oder durch eine nicht kompatible Version ersetzt wurde.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resilienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352489"
---
# <a name="resiliency"></a>Resilienz

Resilienz ist die Fähigkeit einer Anwendung, ordnungsgemäß aus Situationen wiederherzustellen, in denen eine wichtige Komponente fehlt oder durch eine nicht kompatible Version ersetzt wurde. Durch die Erstellung eines Installationspakets und die Verwendung der [Installer-Funktionen](installer-functions.md)können Entwickler die Windows Installer verwenden, um robuste Anwendungen zu erstellen, die aus solchen Situationen wieder hergestellt werden können.

-   Verwenden Sie die Quell Liste des Installers, um die Resilienz von Anwendungen zu erhöhen, die auf Netzwerkressourcen basieren. Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md).
-   Verwenden Sie die-API des Installers, um zu überprüfen, ob ein wichtiges Feature, eine Komponente, eine Datei oder eine Dateiversion installiert ist.
-   Verwenden Sie die-API des Installers, um den Pfad zu einer Komponente zur Laufzeit zu überprüfen. Dadurch wird die Abhängigkeit ihrer Anwendung von statischen Dateipfaden verringert, die sich häufig zwischen den Computern unterscheiden.
-   Verwenden Sie das Installationsprogramm, um beschädigte Verknüpfungen, Registrierungseinträge und andere Komponenten neu zu installieren, ohne Setup erneut ausführen zu müssen.
-   Erhöhen Sie die Resilienz der Installation des Produkts, indem Sie die Roll Back Funktion des Installers aktivieren. Weitere Informationen finden Sie unter [Rollback-Installation](rollback-installation.md).

 

 



