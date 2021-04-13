---
description: Binärdateien von Windows Server 2003 mit Service Pack 1 (SP1) sind kompatibel mit Windows Vista und Windows Server 2008. Allerdings müssen Binärdateien aus früheren Versionen von Windows neu kompiliert werden.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portieren von Sicherungs Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528709"
---
# <a name="porting-backup-applications"></a>Portieren von Sicherungs Anwendungen

Binärdateien von Windows Server 2003 mit Service Pack 1 (SP1) sind kompatibel mit Windows Vista und Windows Server 2008. Allerdings müssen Binärdateien aus früheren Versionen von Windows neu kompiliert werden.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Portieren von Windows XP-Sicherungs Anwendungen auf Windows Vista

Mehrere VSS-Schnittstellen wurden seit Windows XP geändert. Windows XP-Anwendungen müssen mindestens mithilfe von Header Dateien und Bibliotheken aus dem VSS 7,2 SDK oder dem Windows Vista-oder Windows Server 2008 SDK neu kompiliert werden.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Portieren von Windows Server 2003 SP1-Sicherungs Anwendungen auf Windows Vista

Binärdateien von Windows Server 2003 mit SP1 sind kompatibel mit Windows Vista und Windows Server 2008. Die meisten Windows Server 2003 mit SP1-Sicherungs Anwendungen müssen jedoch aktualisiert werden, um neue Features zu berücksichtigen, die in den folgenden Abschnitten beschrieben werden.

## <a name="compiling-backup-applications-for-windows-vista"></a>Kompilieren von Sicherungs Anwendungen für Windows Vista

Anwendungen, die in Windows Server 2003 verfügbare Schnittstellen verwenden, können mithilfe von Header Dateien und Bibliotheken kompiliert werden, die im VSS 7,2 SDK bereitgestellt werden. Zum Verwenden neuer Schnittstellen müssen Anwendungen mithilfe der Header Dateien und Bibliotheken, die im Windows Vista SDK enthalten sind, neu kompiliert werden.

> [!Note]  
> Mit Windows Vista oder Windows Server 2008 kompilierte Binärdateien sind nicht mit Windows Server 2003 mit SP1 oder früheren Windows-Versionen kompatibel.

 

 

 



