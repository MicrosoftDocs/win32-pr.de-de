---
description: 'Bestimmte Funktionen, die für die Windows Server 2003-Version von VSS geplant sind, werden nicht vollständig unterstützt:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Einschränkungen in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198e4ce79da4665bf712a64a466691041d452d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368256"
---
# <a name="restrictions-in-windows-server-2003"></a>Einschränkungen in Windows Server 2003

Bestimmte Funktionen, die für die Windows Server 2003-Version von VSS geplant sind, werden nicht vollständig unterstützt:

-   Während des Sicherungs Vorgangs sind mehrere Instanzen einer bestimmten Writer-Klasse nur zulässig, wenn nur eine dieser Instanzen einen Writer-Wiederherstellungs Status aufweist (siehe VSS-enumerationsenumeration), außer [**\_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)VSS \_ WRE \_ nie. Wenn diese Bedingung erfüllt ist, werden alle Writer-Instanzen während der Sicherung vollständig einbezogen, und es werden Writer-Metadatendokumente erstellt und an der Ereignis Behandlung beteiligt.
-   Während des Wiederherstellungs Vorgangs empfängt nur ein Writer Wiederherstellungs Ereignisse, die vom Anforderer generiert werden. Wenn für mehr als eine Instanz einer Writer-Klasse ein Writer-Wiederherstellungs Status auf einen anderen Wert als VSS WRE festgelegt ist \_ \_ , empfängt nur eine Instanz Wiederherstellungs Ereignisse. Die Instanz, die Sie empfängt, ist unbestimmt.

 

 



