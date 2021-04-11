---
description: Der Windows Installer bestimmt, ob das Entfernen einer Common Language Runtime Assembly basierend auf einer Client Liste zulässig ist, die unabhängig von der Assembly gespeichert wird.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Entfernen von Assemblys aus dem globalen Assemblycache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216033"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Entfernen von Assemblys aus dem globalen Assemblycache

Der Windows Installer bestimmt, ob das Entfernen einer Common Language Runtime Assembly basierend auf einer Client Liste zulässig ist, die unabhängig von der Assembly gespeichert wird. Der Windows Installer behält ein Pin-Bit bei, das Windows Installer Clients der Assembly repräsentiert. Das Installationsprogramm heftet die Assembly für den ersten Windows Installer Client an und entheftet Sie, wenn der letzte Windows Installer Client entfernt wird. Die Assembly verwaltet ein Pin-Bit für jeden Client einer Assembly.

Der Windows Installer ist nicht direkt verantwortlich für das physische Entfernen von Common Language Runtime Assemblys vom Computer. Der Installer entfernt die Assembly, wenn der letzte Windows Installer Client entfernt wird. Wenn die Windows Installer der letzte Client der Assembly ist, stellt die Common Language Runtime die Option bereit, eine synchrone Bereinigung der Assembly zu erzwingen. Der Bereinigungs Prozess ist atomarisch, und an dieser Stelle wird kein "Rollback" bereitgestellt. Alle Assemblys von Common Language Runtime Assemblys müssen auftreten, nachdem der Benutzer die Installation oder Entfernung abgebrochen hat.

 

 



