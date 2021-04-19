---
description: Wenn die msidbcustomaction typecontinue-Rückgabe Verarbeitungsoption nicht festgelegt ist, muss die benutzerdefinierte Aktion einen ganzzahligen Statuscode zurückgeben, wie in der folgenden Tabelle gezeigt.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Rückgabewerte für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363781"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="aebf9-103">Rückgabewerte für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="aebf9-103">Custom Action Return Values</span></span>

<span data-ttu-id="aebf9-104">Wenn die **msidbcustomaction typecontinue** -Rückgabe Verarbeitungsoption nicht festgelegt ist, muss die benutzerdefinierte Aktion einen ganzzahligen Statuscode zurückgeben, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aebf9-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="aebf9-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aebf9-105">Return value</span></span>                 | <span data-ttu-id="aebf9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aebf9-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="aebf9-107">Fehler \_ Funktion \_ nicht \_ aufgerufen</span><span class="sxs-lookup"><span data-stu-id="aebf9-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="aebf9-108">Die Aktion wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aebf9-108">Action not executed.</span></span>                  |
| <span data-ttu-id="aebf9-109">Fehler \_ erfolgreich</span><span class="sxs-lookup"><span data-stu-id="aebf9-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="aebf9-110">Aktionen erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aebf9-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="aebf9-111">Fehler beim \_ Installieren von \_ Userexit.</span><span class="sxs-lookup"><span data-stu-id="aebf9-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="aebf9-112">Der Benutzer wurde vorzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="aebf9-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="aebf9-113">Fehler bei der \_ Installation. \_</span><span class="sxs-lookup"><span data-stu-id="aebf9-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="aebf9-114">Nicht BEHEB barer Fehler.</span><span class="sxs-lookup"><span data-stu-id="aebf9-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="aebf9-115">Fehler \_ keine \_ weiteren \_ Elemente</span><span class="sxs-lookup"><span data-stu-id="aebf9-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="aebf9-116">Überspringen Sie die restlichen Aktionen und keinen Fehler.</span><span class="sxs-lookup"><span data-stu-id="aebf9-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="aebf9-117">Beachten Sie, dass benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, für Erfolg den Wert 0 zurückgeben müssen.</span><span class="sxs-lookup"><span data-stu-id="aebf9-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="aebf9-118">Der Installer interpretiert jeden anderen Rückgabewert als Fehler.</span><span class="sxs-lookup"><span data-stu-id="aebf9-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="aebf9-119">Wenn Sie Rückgabewerte ignorieren möchten, legen Sie das **msidbcustomaction typecontinue** -Bitflag im type-Feld der [CustomAction-Tabelle](customaction-table.md)fest.</span><span class="sxs-lookup"><span data-stu-id="aebf9-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="aebf9-120">Weitere Informationen zur Option " **msidbcustomaction typecontinue** " und anderen Optionen zur Rückgabe Verarbeitung finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="aebf9-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="aebf9-121">Beachten Sie, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="aebf9-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="aebf9-122">Wenn der Rückgabewert der Aktion z. b. als 1 in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion Fehler erfolgreich zurückgegeben hat \_ .</span><span class="sxs-lookup"><span data-stu-id="aebf9-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="aebf9-123">Weitere Informationen zu dieser Übersetzung finden Sie [unter Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="aebf9-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aebf9-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aebf9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aebf9-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="aebf9-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="aebf9-126">Protokollierung von Aktions Rückgabe Werten</span><span class="sxs-lookup"><span data-stu-id="aebf9-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



