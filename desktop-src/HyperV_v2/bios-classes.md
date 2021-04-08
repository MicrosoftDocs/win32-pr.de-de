---
description: Das virtuelle BIOS ist ein Software Abbild, das in den RAM geladen wird, um einige der grundlegenden Aspekte von zu konfigurieren und ein Computersystem zu starten. Es gibt ein BIOS-Element pro Computersystem, und dieses Element kann nicht ersetzt oder entfernt werden.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: BIOS-Klassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959804"
---
# <a name="bios-classes"></a><span data-ttu-id="dd159-104">BIOS-Klassen</span><span class="sxs-lookup"><span data-stu-id="dd159-104">BIOS classes</span></span>

<span data-ttu-id="dd159-105">Das virtuelle BIOS ist ein Software Abbild, das in den RAM geladen wird, um einige der grundlegenden Aspekte von zu konfigurieren und ein Computersystem zu starten.</span><span class="sxs-lookup"><span data-stu-id="dd159-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="dd159-106">Es gibt ein BIOS-Element pro Computersystem, und dieses Element kann nicht ersetzt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="dd159-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="dd159-107">Folglich gibt es keinen Ressourcenpool zum Hinzufügen neuer BIOS-Elemente zum virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="dd159-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="dd159-108">Das BIOS-Element verfügt auch nicht über eine eigene SettingData-Klasse, um die Einstellungen für das BIOS zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="dd159-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="dd159-109">Die Einstellungen für das BIOS (z. b. Seriennummern, Start Reihenfolge und Num-Sperr Status) finden Sie in der Klasse " [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) ".</span><span class="sxs-lookup"><span data-stu-id="dd159-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="dd159-110">Im folgenden finden Sie WMI-Klassen für die Virtualisierung im Zusammenhang mit dem BIOS.</span><span class="sxs-lookup"><span data-stu-id="dd159-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="dd159-111">Diese Klassen befinden sich im \\ \\ . \\ \\Namespace für die stammvirtualisierung.</span><span class="sxs-lookup"><span data-stu-id="dd159-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dd159-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dd159-112">In this section</span></span>



| <span data-ttu-id="dd159-113">Thema</span><span class="sxs-lookup"><span data-stu-id="dd159-113">Topic</span></span>                                                    | <span data-ttu-id="dd159-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd159-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd159-115">**MSVM- \_ bioselements**</span><span class="sxs-lookup"><span data-stu-id="dd159-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="dd159-116">Stellt die Software auf niedriger Ebene dar, die in den RAM geladen wird, um das System zu konfigurieren und zu starten.</span><span class="sxs-lookup"><span data-stu-id="dd159-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="dd159-117">**MSVM- \_ Systembios**</span><span class="sxs-lookup"><span data-stu-id="dd159-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="dd159-118">Wird verwendet, um dem BIOS eine virtuelle Maschine zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dd159-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




