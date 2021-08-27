---
description: 'Bestimmte Funktionen, die für das Windows Server 2003-Release von VSS geplant sind, werden nicht vollständig unterstützt:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Einschränkungen in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7353b2d52a7222015f051e15ba07830b81d6aedda6323bca4378f459eb602ba8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124510"
---
# <a name="restrictions-in-windows-server-2003"></a>Einschränkungen in Windows Server 2003

Bestimmte Funktionen, die für das Windows Server 2003-Release von VSS geplant sind, werden nicht vollständig unterstützt:

-   Während Sicherungsvorgängen sind mehrere Instanzen einer bestimmten Writer-Klasse nur zulässig, wenn nur eine dieser Instanzen über einen Writer-Wiederherstellungsstatus verfügt (siehe [**VSS \_ WRITERRESTORE-ENUM) \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)außer VSS \_ WRE \_ NEVER. Wenn diese Bedingung erfüllt ist, nehmen alle Writerinstanzen während der Sicherung vollständig teil, generieren WriterMetadatendokumente und nehmen an der Ereignisbehandlung teil.
-   Während der Wiederherstellungsvorgänge empfängt nur ein Writer Wiederherstellungsereignisse, die vom Anfordernden generiert werden. Wenn für mehrere Instanzen einer Writer-Klasse ein Writer-Wiederherstellungsstatus auf einen anderen Zustand als VSS WRE NEVER festgelegt \_ \_ ist, empfängt nur eine Instanz Wiederherstellungsereignisse. Welche Instanz sie empfängt, ist unbestimmt.

 

 



