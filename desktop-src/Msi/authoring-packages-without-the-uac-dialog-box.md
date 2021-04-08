---
description: Wenn für die Installation eines Windows Installer Pakets erweiterte Berechtigungen nicht erforderlich sind, kann der Autor des Pakets das von der Benutzerkontensteuerung (User Account Control, UAC) angeforderte Dialogfeld unterdrücken, um Benutzer zur Autorisierung von Administratoren aufzufordern.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Erstellen von Paketen ohne das UAC-Dialog Feld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756229"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="8aac4-103">Erstellen von Paketen ohne das UAC-Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="8aac4-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="8aac4-104">Wenn für die Installation eines Windows Installer Pakets erweiterte Berechtigungen nicht erforderlich sind, kann der Autor des Pakets das von der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) angeforderte Dialogfeld unterdrücken, um Benutzer zur Autorisierung von Administratoren aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="8aac4-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="8aac4-105">Um die Anzeige des Dialog Felds UAC bei der Installation der Anwendung zu unterdrücken, sollte der Autor des Pakets folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="8aac4-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="8aac4-106">Installieren Sie die Anwendung mithilfe von Windows Installer 4,0 oder höher unter Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8aac4-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="8aac4-107">Verwenden Sie keine erhöhten System Privilegien, um die Anwendung auf dem Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8aac4-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="8aac4-108">Installieren Sie die Anwendung im kontextbezogenen Kontext, und legen Sie diesen als Standard Installations Kontext des Pakets ab.</span><span class="sxs-lookup"><span data-stu-id="8aac4-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="8aac4-109">Wenn die Eigenschaft " [**ALLUSERS**](allusers.md) " nicht festgelegt ist, wird das Paket vom Installationsprogramm im benutzerspezifischen Kontext installiert.</span><span class="sxs-lookup"><span data-stu-id="8aac4-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="8aac4-110">Wenn Sie die Eigenschaft **ALLUSERS** nicht in die [Eigenschaften Tabelle](property-table.md)einschließen, wird diese Eigenschaft vom Installer nicht festgelegt, sodass die Installation pro Benutzer zum Standard Installations Kontext wird.</span><span class="sxs-lookup"><span data-stu-id="8aac4-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="8aac4-111">Sie können diesen Standardwert überschreiben, indem Sie die Eigenschaft **ALLUSERS** in der Befehlszeile festlegen.</span><span class="sxs-lookup"><span data-stu-id="8aac4-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="8aac4-112">Legen Sie in der Eigenschaft [**Wort Zähl Zusammenfassung**](word-count-summary.md) den Wert Bit 3 fest, um anzugeben, dass für die Installation der Anwendung keine erhöhten Rechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8aac4-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



