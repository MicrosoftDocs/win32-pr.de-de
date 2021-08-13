---
description: Paketautoren können interne Windows Installer-Meldungen durch die Erstellung einer ausführbaren Anwendung überwachen, die sowohl einen Rückrufhandler zum Empfangen der Nachrichten als auch funktionen zum Initiieren einer Installation enthält.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Überwachen einer Installation mit msiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660b1454d7e4f3437da6dce41707a1516207d853510e8475837f31e60090b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628571"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a>Überwachen einer Installation mit msiSetExternalUI

Paketautoren können interne Windows Installer-Meldungen durch die Erstellung einer ausführbaren Anwendung überwachen, die sowohl einen Rückrufhandler zum Empfangen der Nachrichten als auch funktionen zum Initiieren einer Installation enthält.

Der Rückrufhandler entspricht dem INSTALLUI HANDLER-Prototyp, und ein Zeiger auf diesen Rückrufhandler wird an \_ [**MsiSetExternalUI übergeben.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) Nachdem die Installation durch einen Aufruf von [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)initiiert wurde, werden Installationsmeldungen vom Rückrufhandler abgefangen, und der Paketautor kann diese Nachrichten selektiv anzeigen oder ignorieren.

Weitere Informationen finden Sie unter Handling [Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External Benutzeroberfläche Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).

Weitere Informationen zur Verwendung eines datensatzbasierten externen Handlers finden Sie unter [Überwachen einer Installation mit msiSetExternalUIRecord.](monitoring-an-installation-using-msisetexternaluirecord.md)

 

 



