---
description: Im folgenden Verfahren wird beschrieben, wie parallele Assemblys als freigegebene Assemblys installiert werden.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installieren paralleler Assemblys als freigegebene Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484643"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Installieren paralleler Assemblys als freigegebene Assemblys

Im folgenden Verfahren wird beschrieben, wie parallele Assemblys als [frei](about-side-by-side-assemblies-.md) [gegebene](/windows/desktop/Msi/shared-assemblies)Assemblys installiert werden.

**So installieren Sie eine parallele Assembly als freigegebene Assembly**

1.  Signieren Sie einen Katalog für die Dateien in der Assembly, und erstellen Sie ihn.

    Dateien müssen signiert werden, damit Sie als parallele Assemblys installiert werden. Weitere Informationen finden Sie [unter Erstellen signierter Dateien und Kataloge](creating-signed-files-and-catalogs.md).

2.  Sie sollten freigegebene parallele Assemblys als Komponenten eines Windows Installer Pakets installieren. Dabei kann es sich um das Installationspaket handeln, mit dem die Anwendung installiert oder aktualisiert wird. Wenn die freigegebene Assembly als Teil mehrerer Anwendungen ausgeliefert wird, sollten Sie ein Mergemodul bereitstellen, das in die Installationspakete dieser Anwendungen eingebunden werden kann, und einen Katalog für die Dateien in der Assembly erstellen.

    Zum Installieren von Assemblys ist Windows Installer Version 2,0 oder höher erforderlich. Weitere Informationen finden Sie im [Windows Installer](../msi/windows-installer-portal.md) SDK und in den Abschnitten unter [Installieren von Win32](../msi/installation-of-win32-assemblies.md)-Assemblys.

 

 
