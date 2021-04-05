---
description: Entwickler können verhindern, dass vertrauliche Informationen (z. b. Kenn Wörter) während einer Windows Installer-Installation in die Protokolldatei eingegeben werden.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042140"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="bb9ad-103">Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden</span><span class="sxs-lookup"><span data-stu-id="bb9ad-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="bb9ad-104">Wenn Sie die Windows Installer verwenden, können Sie verhindern, dass vertrauliche Informationen, z. b. Kenn Wörter, in die Protokolldatei eingegeben und sichtbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="bb9ad-105">Das Installationsprogramm schreibt die Informationen in der Spalte Kennwort der [Tabelle ServiceInstall](serviceinstall-table.md) niemals in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="bb9ad-106">Sie können verhindern, dass das Installationsprogramm die Eigenschaft, die mit einem [Bearbeitungs Steuer](edit-control.md) Element verknüpft ist, in das Protokoll schreibt, indem Sie das Kenn [Wort Steuerungs Attribut](password-control-attribute.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="bb9ad-107">Die Eigenschaft, die mit einem Bearbeitungs Steuerelement verknüpft ist, das über das Kenn Wort Steuerelement-Attribut verfügt, wird ausgeblendet, auch wenn die [debugrichtlinie](debug.md) auf den Wert 7 festgelegt</span><span class="sxs-lookup"><span data-stu-id="bb9ad-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="bb9ad-108">Sie können verhindern, dass das Installationsprogramm eine private-Eigenschaft in das Protokoll schreibt, indem Sie die-Eigenschaft in die [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft einschließen.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="bb9ad-109">Mit dieser Methode können vertrauliche Informationen in einer Befehlszeile eingegeben werden, die im Protokoll sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="bb9ad-110">Wenn die [debugrichtlinie](debug.md) auf den Wert 7 festgelegt ist, schreibt das Installationsprogramm Informationen, die in der Befehlszeile eingegeben werden, in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="bb9ad-111">Dadurch wird die Eigenschaft, die in einer Befehlszeile eingegeben wird, auch dann sichtbar, wenn die Eigenschaft in der [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="bb9ad-112">Sie können verhindern, dass die Informationen in der Ziel Spalte der Tabelle [CustomAction](customaction-table.md) in das Protokoll geschrieben werden, indem Sie das hidetarget-Bitflag in das type-Feld der CustomAction-Tabelle einschließen.</span><span class="sxs-lookup"><span data-stu-id="bb9ad-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="bb9ad-113">Der Wert dieses Flags ist 8192 (0x2000).</span><span class="sxs-lookup"><span data-stu-id="bb9ad-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="bb9ad-114">Weitere Informationen finden Sie unter Option für ausgeblendete [Ziel benutzerdefinierte Aktionen](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="bb9ad-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



