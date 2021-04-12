---
description: Desktop der HKCU \\ -Systemsteuerung \\
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393158"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="5165c-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="5165c-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="5165c-104">**Desktop der HKCU \\ -Systemsteuerung \\**</span><span class="sxs-lookup"><span data-stu-id="5165c-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="5165c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5165c-105">Data type</span></span> | <span data-ttu-id="5165c-106">Range</span><span class="sxs-lookup"><span data-stu-id="5165c-106">Range</span></span>       | <span data-ttu-id="5165c-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="5165c-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="5165c-108">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5165c-108">REG\_SZ</span></span>   | <span data-ttu-id="5165c-109">*Dateiname*</span><span class="sxs-lookup"><span data-stu-id="5165c-109">*File name*</span></span> | <span data-ttu-id="5165c-110">(Keine)</span><span class="sxs-lookup"><span data-stu-id="5165c-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="5165c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5165c-111">Description</span></span>

<span data-ttu-id="5165c-112">Gibt den Namen der ausführbaren Datei für den Bildschirmschoner an.</span><span class="sxs-lookup"><span data-stu-id="5165c-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="5165c-113">Methode ändern</span><span class="sxs-lookup"><span data-stu-id="5165c-113">Change Method</span></span>

<span data-ttu-id="5165c-114">Um den Wert dieses Eintrags zu ändern, doppelklicken Sie in der Systemsteuerung auf **Anzeige**, klicken Sie auf die Registerkarte **Bildschirmschoner** , und wählen Sie dann in der Liste **Bildschirmschoner** einen Bildschirmschoner aus.</span><span class="sxs-lookup"><span data-stu-id="5165c-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="5165c-115">Sie können diesen Eintrag auch mit der API-Funktion (Application Programming Interface, Anwendungsprogrammierschnittstelle) ändern, die von Desk.cpl **exportiert wird.**</span><span class="sxs-lookup"><span data-stu-id="5165c-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="5165c-116">Sie können auf diese Funktion mit der Befehlszeile **rundll32.exe desk.cpl, installbildschirm** *Datei* zugreifen, wobei *File* der Name einer ausführbaren Datei für Bildschirmschoner ist.</span><span class="sxs-lookup"><span data-stu-id="5165c-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="5165c-117">Aktivierungsmethoden</span><span class="sxs-lookup"><span data-stu-id="5165c-117">Activation Method</span></span>

<span data-ttu-id="5165c-118">Änderungen, die an diesem Eintrag vorgenommen werden, werden wirksam, wenn das System den Bildschirmschoner das nächste Mal startet.</span><span class="sxs-lookup"><span data-stu-id="5165c-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="5165c-119">Änderungen, die an diesem Eintrag vorgenommen werden, während ein Bildschirmschoner ausgeführt wird, wirken sich nicht auf die Ausführung des Bildschirmschoners aus.</span><span class="sxs-lookup"><span data-stu-id="5165c-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="5165c-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="5165c-120">Notes</span></span>

-   <span data-ttu-id="5165c-121">Windows-Betriebssysteme fügen diesen Eintrag zur Registrierung hinzu, wenn Sie in der Systemsteuerung **anzeigen** verwenden, um einen Bildschirmschoner auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5165c-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="5165c-122">Wenn Sie alle Bildschirmschoner deaktivieren, indem Sie in der Liste Bildschirmschoner den Eintrag **(keine)** auswählen, löscht das Betriebssystem diesen Eintrag aus der Registrierung und ruft die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit *uiaction* gleich SPI \_ setscreensaveactive und *uiparam* gleich **false** auf.</span><span class="sxs-lookup"><span data-stu-id="5165c-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="5165c-123">Dieser Eintrag kann durch eine Gruppenrichtlinie Einstellung auf Systemen ersetzt werden, die Gruppenrichtlinie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5165c-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="5165c-124">Während der **Name der ausführbaren Datei für den Bildschirmschoner** Gruppenrichtlinie Einstellung aktiviert ist, wird dieser Eintrag vom System ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5165c-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="5165c-125">Die Konfiguration dieser Richtlinien Einstellung wird im **SCRNSAVE.EXE** Eintrag gespeichert, der sich im Unterschlüssel " **Richtlinien** " befindet.</span><span class="sxs-lookup"><span data-stu-id="5165c-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
