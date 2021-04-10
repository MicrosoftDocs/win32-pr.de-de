---
title: Abrufen des Status eines Neustart-Manager-Vorgangs
description: Wenn viele Anwendungen und Dienste heruntergefahren oder neu gestartet werden müssen, kann der Neustart-Manager-Vorgang eine längere Zeit in Anspruch nehmen. Die folgende Methode kann verwendet werden, um den Status des aktuellen Vorgangs abzurufen.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102175"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Abrufen des Status eines Neustart-Manager-Vorgangs

Wenn viele Anwendungen und Dienste heruntergefahren oder neu gestartet werden müssen, kann der Neustart-Manager-Vorgang eine längere Zeit in Anspruch nehmen. Die folgende Methode kann verwendet werden, um den Status des aktuellen Vorgangs abzurufen.

**So erhalten Sie den Status des aktuellen Vorgangs zum Neustart-Manager**

1.  Das Installationsprogramm sollte eine [**RM- \_ Schreib \_ Status- \_ Rückruf**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) Funktion implementieren, die den Status der herunter gefahrenen oder neu gestarteten Anwendungen bestimmt. Die-Funktion kann die Informationen für die Benutzeroberfläche oder das Protokoll bereitstellen.
2.  Das Installationsprogramm übergibt den Zeiger an die [**RM- \_ Schreib Status- \_ \_ Rückruf**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) Funktion, wenn die Funktion [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) oder [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) aufgerufen wird.

 

 