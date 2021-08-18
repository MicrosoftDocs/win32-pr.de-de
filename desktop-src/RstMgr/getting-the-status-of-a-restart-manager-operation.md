---
title: Abrufen des Status eines Neustart-Manager-Vorgangs
description: Wenn viele Anwendungen und Dienste heruntergefahren oder neu gestartet werden müssen, kann der Neustart-Manager-Vorgang einen längeren Zeitraum in Anspruch nehmen. Die folgende Methode kann verwendet werden, um den Status des aktuellen Vorgangs abzurufen.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96b7e247bdeb661e29d39cbb64bd8b7aaaa5caf9478bd1f1acc483c1dfbd614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010188"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Abrufen des Status eines Neustart-Manager-Vorgangs

Wenn viele Anwendungen und Dienste heruntergefahren oder neu gestartet werden müssen, kann der Neustart-Manager-Vorgang einen längeren Zeitraum in Anspruch nehmen. Die folgende Methode kann verwendet werden, um den Status des aktuellen Vorgangs abzurufen.

**So erhalten Sie den Status des aktuellen Neustart-Manager-Vorgangs**

1.  Das Installationsprogramm sollte eine [**RM \_ WRITE STATUS \_ \_ CALLBACK-Funktion**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) implementieren, die den Status der Anwendungen bestimmt, die heruntergefahren oder neu gestartet wurden. Die Funktion kann die Informationen für die Benutzeroberfläche oder das Protokoll bereitstellen.
2.  Das Installationsprogramm übergibt beim Aufrufen der [**RmShutdown-**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) oder [**RmRestart-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) den Zeiger auf die [**RM WRITE STATUS \_ \_ \_ CALLBACK-Funktion.**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback)

 

 