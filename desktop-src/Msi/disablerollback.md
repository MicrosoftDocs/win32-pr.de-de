---
description: Wenn diese Systemrichtlinie auf 1 festgelegt ist, werden im Installationsprogramm keine Rollbackdateien während der Installation gespeichert, und das Installationsrollback wird deaktiviert.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da8380ce5dc7ea0b711d5766a554d6dce970bc81587a75164e61f3694c6a5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947314"
---
# <a name="disablerollback"></a>DisableRollback

Wenn diese [Systemrichtlinie](system-policy.md) auf 1 festgelegt ist, werden im Installationsprogramm keine Rollbackdateien während der Installation gespeichert, und das Installationsrollback wird deaktiviert. Standardmäßig ist ein Rollback aktiviert. Administratoren wird empfohlen, diese Richtlinie nur zu verwenden, wenn sie unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Rollbackinstallation](rollback-installation.md).

## <a name="registry-key"></a>Registrierungsschlüssel

Um das Rollback für benutzerspezifische Installationen zu deaktivieren, legen **Sie DisableRollback** unter dem folgenden Registrierungsschlüssel auf 1 fest:

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

Um das Rollback für Computerinstallationen zu deaktivieren, legen **Sie DisableRollback** unter dem folgenden Registrierungsschlüssel auf 1 fest.

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



