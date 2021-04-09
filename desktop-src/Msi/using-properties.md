---
description: In den folgenden Abschnitten wird beschrieben, wie die integrierten Installer-Eigenschaften und zusätzlichen Eigenschaften, die vom Paket Autor definiert werden, verwendet werden.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Verwenden von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129360"
---
# <a name="using-properties"></a><span data-ttu-id="0b4ec-103">Verwenden von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b4ec-103">Using Properties</span></span>

<span data-ttu-id="0b4ec-104">In den folgenden Abschnitten wird beschrieben, wie die integrierten Installer-Eigenschaften und zusätzlichen Eigenschaften, die vom Paket Autor definiert werden, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="0b4ec-105">Eigenschaften können entweder [öffentliche Eigenschaften](public-properties.md) oder [private Eigenschaften](private-properties.md)sein.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="0b4ec-106">Jede Eigenschaft, die bei der Initialisierung des Installers definiert werden muss, muss den Namen und den Anfangswert in der [Eigenschaften Tabelle](property-table.md)auflisten.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="0b4ec-107">Eigenschaften, die einen NULL-Wert haben, sind nicht in der Eigenschaften Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="0b4ec-108">Sie können Eigenschaften aus Programmen und benutzerdefinierten Aktionen erhalten oder festlegen und öffentliche Eigenschaften über die Befehlszeile festlegen.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="0b4ec-109">Der Installationsvorgang kann mithilfe von Eigenschaften in bedingten Anweisungen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="0b4ec-110">Einschränkungen für Eigenschaftsnamen</span><span class="sxs-lookup"><span data-stu-id="0b4ec-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="0b4ec-111">Initialisierung von Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="0b4ec-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="0b4ec-112">Eigenschaften werden erhalten und festgelegt</span><span class="sxs-lookup"><span data-stu-id="0b4ec-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="0b4ec-113">Verwenden von Eigenschaften in Bedingungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0b4ec-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="0b4ec-114">Verwenden einer Verzeichnis Eigenschaft in einem Pfad</span><span class="sxs-lookup"><span data-stu-id="0b4ec-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="0b4ec-115">Verwenden Sie keine Eigenschaften für Kenn Wörter oder andere Informationen, die sicher bleiben müssen.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="0b4ec-116">Das Installationsprogramm kann den Wert einer Eigenschaft, die in die Eigenschaften Tabelle geschrieben oder zur Laufzeit erstellt wurde, in ein Protokoll oder die Systemregistrierung schreiben.</span><span class="sxs-lookup"><span data-stu-id="0b4ec-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0b4ec-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b4ec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b4ec-118">Informationen zu Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b4ec-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="0b4ec-119">Eigenschafts Verweis</span><span class="sxs-lookup"><span data-stu-id="0b4ec-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



