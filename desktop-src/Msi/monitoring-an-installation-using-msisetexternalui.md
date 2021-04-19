---
description: Paket Autoren können interne Windows Installer Meldungen durch die Erstellung einer ausführbaren Anwendung überwachen, die sowohl einen Rückruf Handler zum Empfangen von Nachrichten als auch Funktionen zum Initiieren einer Installation enthält.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Überwachen einer Installation mithilfe von "msieintexternalui"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366168"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a><span data-ttu-id="38481-103">Überwachen einer Installation mithilfe von "msieintexternalui"</span><span class="sxs-lookup"><span data-stu-id="38481-103">Monitoring an Installation Using MsiSetExternalUI</span></span>

<span data-ttu-id="38481-104">Paket Autoren können interne Windows Installer Meldungen durch die Erstellung einer ausführbaren Anwendung überwachen, die sowohl einen Rückruf Handler zum Empfangen von Nachrichten als auch Funktionen zum Initiieren einer Installation enthält.</span><span class="sxs-lookup"><span data-stu-id="38481-104">Package authors can monitor internal Windows Installer messages through the creation of an executable application that contains both a callback handler to receive the messages and functionality to initiate an installation.</span></span>

<span data-ttu-id="38481-105">Der Rückruf Handler entspricht dem installui \_ -handlerprototyp, und ein Zeiger auf diesen Rückruf Handler wird an [**msiabtexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="38481-105">The callback handler conforms to the INSTALLUI\_HANDLER prototype, and a pointer to this callback handler is passed to [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia).</span></span> <span data-ttu-id="38481-106">Nachdem die Installation durch einen [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)-Rückruf initiiert wurde, werden die Installations Meldungen vom Rückruf Handler aufgezeichnet, und der Paket Ersteller kann beliebige oder alle dieser Nachrichten selektiv anzeigen oder ignorieren.</span><span class="sxs-lookup"><span data-stu-id="38481-106">Once the installation has been initiated by a call to [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), installation messages are trapped by the callback handler and the package author can selectively display or ignore any or all of these messages.</span></span>

<span data-ttu-id="38481-107">Weitere Informationen finden Sie unter [Verarbeiten von Statusmeldungen mithilfe von "msieintexternalui](handling-progress-messages-using-msisetexternalui.md)", [zurückgeben von Werten von einem externen Benutzerschnittstellen Handler](returning-values-from-an-external-user-interface-handler.md)und [Windows Installer von Meldungen](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="38481-107">For more information, see [Handling Progress Messages Using MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [Returning Values from an External User Interface Handler](returning-values-from-an-external-user-interface-handler.md), and [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="38481-108">Weitere Informationen zum Verwenden eines Daten Satz basierten externen Handlers finden Sie unter über [Wachen einer Installation mithilfe von "msieintexternaluirecord](monitoring-an-installation-using-msisetexternaluirecord.md)".</span><span class="sxs-lookup"><span data-stu-id="38481-108">For more information about using a record-based external handler, see [Monitoring an Installation Using MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).</span></span>

 

 



