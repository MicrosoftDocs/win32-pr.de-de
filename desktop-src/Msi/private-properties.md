---
description: Private Eigenschaften werden intern vom Installationsprogramm verwendet, und ihre Werte müssen vom Autor des Installationspakets in die Datenbank eingegeben oder vom Installationsprogramm während der Installation auf von der Betriebsumgebung festgelegte Werte festgelegt werden.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Private Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352427"
---
# <a name="private-properties"></a><span data-ttu-id="ba621-103">Private Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba621-103">Private Properties</span></span>

<span data-ttu-id="ba621-104">Private Eigenschaften werden intern vom Installationsprogramm verwendet, und ihre Werte müssen vom Autor des Installationspakets in die Datenbank eingegeben oder vom Installationsprogramm während der Installation auf von der Betriebsumgebung festgelegte Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ba621-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="ba621-105">Der einzige Weg, mit dem Benutzer mit privaten Eigenschaften interagieren können, ist die [Steuerung von Ereignissen](control-events.md) in der erstellten Benutzeroberfläche des Pakets.</span><span class="sxs-lookup"><span data-stu-id="ba621-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="ba621-106">Private Eigenschaftsnamen müssen Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba621-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="ba621-107">Siehe [Einschränkungen für Eigenschaftsnamen](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="ba621-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="ba621-108">Private Eigenschaften beschreiben häufig die Betriebsumgebung.</span><span class="sxs-lookup"><span data-stu-id="ba621-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="ba621-109">Wenn die Installation z. b. auf einer Windows-Plattform ausgeführt wird, legt das Installationsprogramm die [**windowsfolder**](windowsfolder.md) -Eigenschaft auf den in der Eigenschaften Tabelle angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="ba621-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="ba621-110">Private Eigenschaftswerte können nicht in einer Befehlszeile überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ba621-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="ba621-111">Um eine private Eigenschaft aus einer Installation zu löschen, lassen Sie Sie aus der [Eigenschaften Tabelle](property-table.md)aus.</span><span class="sxs-lookup"><span data-stu-id="ba621-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="ba621-112">Unter Windows XP und Windows 2000 können Sie keine private-Eigenschaft in der Benutzeroberflächen Phase der Installation festlegen und dann den Wert an die Ausführungsphase übergeben.</span><span class="sxs-lookup"><span data-stu-id="ba621-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="ba621-113">Eine Liste aller privaten Standardeigenschaften, die vom Installationsprogramm verwendet werden, finden Sie unter [Eigenschafts Referenz](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ba621-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="ba621-114">Sie können eine benutzerdefinierte private Eigenschaft definieren, indem Sie den Eigenschaftsnamen und den Anfangswert in der Eigenschaften Tabelle eingeben.</span><span class="sxs-lookup"><span data-stu-id="ba621-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="ba621-115">Private Eigenschaftsnamen müssen immer Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba621-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba621-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba621-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba621-117">Öffentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba621-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



