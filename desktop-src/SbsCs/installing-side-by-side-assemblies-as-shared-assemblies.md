---
description: Im folgenden Verfahren wird beschrieben, wie Sie nebenseitige Assemblys als freigegebene Assemblys installieren.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installieren von nebenseitigen Assemblys als freigegebene Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6348354b224e281135e72697aaa155ce69f4ccd23293f671d733e2bc1cd89dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127510"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Installieren von nebenseitigen Assemblys als freigegebene Assemblys

Im folgenden Verfahren wird beschrieben, wie Sie [nebenseitige](about-side-by-side-assemblies-.md) Assemblys als freigegebene [Assemblys installieren.](/windows/desktop/Msi/shared-assemblies)

**So installieren Sie eine side-by-side-Assembly als freigegebene Assembly**

1.  Signieren Und erstellen Sie einen Katalog für die Dateien in der Assembly.

    Dateien müssen signiert werden, um sie als side-by-side-Assemblys zu installieren. Weitere Informationen finden Sie unter [Erstellen signierter Dateien und Kataloge.](creating-signed-files-and-catalogs.md)

2.  Sie sollten freigegebene, nebenseitige Assemblys als Komponenten eines Pakets Windows Installer installieren. Dies kann das gleiche Installationspaket sein, das zum Installieren oder Aktualisieren Ihrer Anwendung verwendet wird. Wenn die freigegebene Assembly als Teil mehrerer Anwendungen ausgeliefert wird, sollten Sie ein Mergemodul bereitstellen, das in die Installationspakete dieser Anwendungen integriert werden kann, und einen Katalog für die Dateien in der Assembly erstellen.

    Windows Installationsprogramm version 2.0 oder höher ist erforderlich, um Assemblys zu installieren. Weitere Informationen finden Sie im Windows [Installer](../msi/windows-installer-portal.md) SDK und in den Abschnitten unter [Installation von Win32-Assemblys.](../msi/installation-of-win32-assemblies.md)

 

 
