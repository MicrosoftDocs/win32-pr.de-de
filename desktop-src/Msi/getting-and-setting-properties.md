---
description: Wenn Sie Eigenschaften in der-Installation verwenden möchten, können Sie Eigenschaftswerte mithilfe von "MsiGetProperty" und "msisetproperty" aus Programmen aufrufen und festlegen und als Teil von Bedingungs Anweisungen in die-Installations Datenbank einschließen.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Festlegen und Festlegen von Eigenschaften (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866328"
---
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="e9210-103">Festlegen und Festlegen von Eigenschaften (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="e9210-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="e9210-104">Wenn Sie [Eigenschaften](properties.md) in der-Installation verwenden möchten, können Sie Eigenschaftswerte mithilfe von " [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) " und " [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) " aus Programmen aufrufen und festlegen und als Teil von Bedingungs Anweisungen in die-Installations Datenbank einschließen.</span><span class="sxs-lookup"><span data-stu-id="e9210-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="e9210-105">Rufen Sie zum Abrufen einer aktuellen Eigenschaft die [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="e9210-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="e9210-106">Rufen Sie zum Abrufen des aktuellen Installationsstatus die [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="e9210-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="e9210-107">Rufen Sie zum Abrufen der Sprache für die aktuelle Installation die [**msigetlanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="e9210-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="e9210-108">Um eine Eigenschaft festzulegen, müssen Sie die [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e9210-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="e9210-109">Um den Installationsstatus festzulegen, müssen Sie die [**msisetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e9210-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="e9210-110">Um eine Eigenschaft zu löschen (auf NULL festzulegen), legen Sie den Wert der Eigenschaft auf eine leere Zeichenfolge fest: "".</span><span class="sxs-lookup"><span data-stu-id="e9210-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9210-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9210-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9210-112">Verwenden von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9210-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="e9210-113">Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="e9210-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="e9210-114">Löschen einer installereigenschaft</span><span class="sxs-lookup"><span data-stu-id="e9210-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 



