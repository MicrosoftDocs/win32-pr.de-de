---
description: Verwenden Sie die folgenden Optionsflags, um anzugeben, dass das Installationsprogramm den Wert, der in das Zielfeld der CustomAction-Tabelle eingegeben wurde, nicht in das Protokoll schreibt. Legen Sie zum Festlegen der Option den Wert in dieser Tabelle dem Wert im type-Feld der CustomAction-Tabelle hinzu.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Option "ausgeblendetes Ziel"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042399"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="bd59c-104">Option "ausgeblendetes Ziel"</span><span class="sxs-lookup"><span data-stu-id="bd59c-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="bd59c-105">Verwenden Sie die folgenden Optionsflags, um anzugeben, dass das Installationsprogramm den Wert, der in das Zielfeld der [CustomAction-Tabelle](customaction-table.md) eingegeben wurde, nicht in das Protokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="bd59c-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="bd59c-106">Legen Sie zum Festlegen der Option den Wert in dieser Tabelle dem Wert im type-Feld der CustomAction-Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="bd59c-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="bd59c-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="bd59c-107">Constant</span></span>                            | <span data-ttu-id="bd59c-108">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="bd59c-108">Hexadecimal</span></span> | <span data-ttu-id="bd59c-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="bd59c-109">Decimal</span></span> | <span data-ttu-id="bd59c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd59c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd59c-111">(none)</span><span class="sxs-lookup"><span data-stu-id="bd59c-111">(none)</span></span>                              | <span data-ttu-id="bd59c-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="bd59c-112">0x0000</span></span>      | <span data-ttu-id="bd59c-113">0</span><span class="sxs-lookup"><span data-stu-id="bd59c-113">0</span></span>       | <span data-ttu-id="bd59c-114">Der Installer kann den Wert in der Ziel Spalte der CustomAction-Tabelle in die Protokolldatei schreiben.</span><span class="sxs-lookup"><span data-stu-id="bd59c-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="bd59c-115">**msidbcustomaktiontypehidetarget**</span><span class="sxs-lookup"><span data-stu-id="bd59c-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="bd59c-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="bd59c-116">0x2000</span></span>      | <span data-ttu-id="bd59c-117">8192</span><span class="sxs-lookup"><span data-stu-id="bd59c-117">8192</span></span>    | <span data-ttu-id="bd59c-118">Das Installationsprogramm wird daran gehindert, den Wert in der Ziel Spalte der [CustomAction-Tabelle](customaction-table.md) in die Protokolldatei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="bd59c-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="bd59c-119">Die CustomAction Data-Eigenschaft wird auch nicht protokolliert, wenn das Installationsprogramm die benutzerdefinierte Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="bd59c-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="bd59c-120">Da das Installationsprogramm den Wert von CustomAction Data aus einer Eigenschaft mit demselben Namen wie die benutzerdefinierte Aktion festlegt, muss diese Eigenschaft in der Eigenschaft [**msihiddenproperties**](msihiddenproperties.md) aufgeführt werden, um zu verhindern, dass der Wert im Protokoll angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bd59c-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="bd59c-121">Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="bd59c-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd59c-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd59c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd59c-123">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="bd59c-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="bd59c-124">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="bd59c-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="bd59c-125">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="bd59c-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




