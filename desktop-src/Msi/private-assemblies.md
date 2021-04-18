---
description: Eine Win32-Assembly kann als private Assembly installiert und exklusiv für eine Anwendung verwendet werden. Private Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Private Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216356"
---
# <a name="private-assemblies"></a>Private Assemblys

Eine Win32-Assembly kann als private Assembly installiert und exklusiv für eine Anwendung verwendet werden. Private Assemblys sollten von einem Windows Installer Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.

Unter Windows XP werden private Assemblys als [parallele](side-by-side-assemblies.md)Assemblys installiert. Der Windows Installer installiert private parallele Assemblys in einem Ordner, der für die Anwendung privat ist. Üblicherweise der Ordner, der die ausführbare Datei der Anwendung enthält. Die Abhängigkeit der Anwendung auf dem private Assembly wird in einer Anwendungs Manifest-Datei angegeben. Weitere Informationen finden Sie unter [isolierte Anwendungen und](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)parallele Assemblys.

Auf älteren Betriebssystemen als Windows XP wird eine Kopie der private Assembly und einer lokalen Datei in einem privaten Ordner installiert, um die Anwendung exklusiv zu verwenden. Eine Version der Assembly wird auch global auf dem System registriert und steht für jede Anwendung zur Verfügung, die Sie bindet. Die globale Version der Assembly kann die Version sein, die mit der Anwendung installiert wird, oder eine frühere Version. Die globale Version wird durch die gleichen Regeln festgelegt, die von [isolierten Komponenten](isolated-components.md)verwendet werden.

Beachten Sie, dass die Windows Installer eine private Assembly nicht an einem Speicherort mit einem Pfad mit mehr als 234 Zeichen installieren kann, einschließlich des abschließenden NULL-Zeichens.

 

 
