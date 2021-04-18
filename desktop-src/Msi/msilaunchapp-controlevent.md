---
description: Dieses Steuerungs Ereignis führt eine angegebene Datei aus. Wenn die Datei nicht vorhanden ist oder das Ereignis fehlschlägt, protokolliert Windows Installer den Fehler im ausführlichen Protokoll, ohne dass ein Dialogfeld mit einer Fehlermeldung angezeigt wird.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: Msilaunchapp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347296"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="fec97-104">Msilaunchapp ControlEvent</span><span class="sxs-lookup"><span data-stu-id="fec97-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="fec97-105">Dieses Steuerungs Ereignis führt eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="fec97-105">This control event runs a specified file.</span></span> <span data-ttu-id="fec97-106">Wenn die Datei nicht vorhanden ist oder das Ereignis fehlschlägt, protokolliert Windows Installer den Fehler im ausführlichen Protokoll, ohne dass ein Dialogfeld mit einer Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fec97-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="fec97-107">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fec97-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="fec97-108">Dieses ControlEvent ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fec97-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="fec97-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="fec97-109">Published By</span></span>

<span data-ttu-id="fec97-110">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="fec97-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="fec97-111">Argument</span><span class="sxs-lookup"><span data-stu-id="fec97-111">Argument</span></span>

<span data-ttu-id="fec97-112">Die Felder des Argument Werts sind durch Leerzeichen begrenzt.</span><span class="sxs-lookup"><span data-stu-id="fec97-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="fec97-113">Das erste Feld enthält einen Zeichen folgen Wert, der die Datei angibt, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fec97-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="fec97-114">Verwenden Sie den Zeichen folgen Wert \[ \# *filekey* \] , um die Datei zu identifizieren und *filekey* durch den Bezeichner der Datei zu ersetzen, der in der Datei Spalte der [Datei](file-table.md) Tabelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fec97-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="fec97-115">Alle verbleibenden Felder des Arguments können Parameter enthalten, die von der Datei verwendet werden, die ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fec97-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="fec97-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="fec97-116">Action on Subscribers</span></span>

<span data-ttu-id="fec97-117">Diese ControlEvent führt keine Aktionen für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="fec97-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="fec97-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="fec97-118">Typical Use</span></span>

<span data-ttu-id="fec97-119">, Um es einem Benutzer zu ermöglichen, eine Datei am Ende einer-Installation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fec97-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="fec97-120">Dieses Ereignis kann auf eine Eigenschaft festgelegt werden, die durch ein [CheckBox](checkbox-control.md) -Steuerelement festgelegt wird, das im abschließenden Dialogfeld der Installation angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fec97-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="fec97-121">Beim Entfernen des Pakets sollte das CheckBox-Steuerelement nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fec97-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



