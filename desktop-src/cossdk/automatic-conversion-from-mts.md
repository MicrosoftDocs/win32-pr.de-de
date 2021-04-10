---
description: Automatische Konvertierung von MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Automatische Konvertierung von MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127165"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="68d6e-103">Automatische Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="68d6e-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="68d6e-104">Die automatische Konvertierung erfolgt in zwei Schritten:</span><span class="sxs-lookup"><span data-stu-id="68d6e-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="68d6e-105">Während des Windows-Setups.</span><span class="sxs-lookup"><span data-stu-id="68d6e-105">During Windows setup.</span></span> <span data-ttu-id="68d6e-106">Die Konvertierung erfolgt durch den Windows-Setup Vorgang über das Dienstprogramm "mtstocom".</span><span class="sxs-lookup"><span data-stu-id="68d6e-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="68d6e-107">Wenn Schritt 1 fehlschlägt, wurden möglicherweise einige oder alle der MTS-Pakete konvertiert, aber möglicherweise fehlen bestimmte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68d6e-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="68d6e-108">Verwenden Sie in diesem Fall das Verwaltungs Programmkomponenten Dienste, um alle Attribute zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="68d6e-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="68d6e-109">Die MTS-Attribute sind weiterhin auf dem Computer vorhanden (in der Systemregistrierung auf dem lokalen HKEY-Computer \_ \_ \\ Microsoft \\ Transaction Server), sind jedoch nur über das regedit.exe-Hilfsprogramm zugänglich.</span><span class="sxs-lookup"><span data-stu-id="68d6e-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="68d6e-110">Nach dem letzten Neustart, bevor das Windows-Anmelde Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="68d6e-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="68d6e-111">In Schritt 2 werden diese Konvertierungs Aktionen behandelt, die den Netzwerk Zugriff erfordern (hauptsächlich Erstellung von Rollen Mitgliedern).</span><span class="sxs-lookup"><span data-stu-id="68d6e-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="68d6e-112">Wenn Schritt 2 fehlschlägt (aufgrund von temporären Netzwerk-oder Domänen Controller Fehlern), ist es möglich, das mtstocom-Konvertierungsprogramm beliebig oft erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="68d6e-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="68d6e-113">Geben Sie dazu an der Eingabeaufforderung oder nach der Auswahl von **Ausführen** im **Startmenü** Folgendes ein: **% windir% \\ system32 \\mtstocom.exe**.</span><span class="sxs-lookup"><span data-stu-id="68d6e-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="68d6e-114">Mtstocom-Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="68d6e-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="68d6e-115">Das Dienstprogramm mtstocom generiert eine Protokolldatei (mtstocom. log) im Windows-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="68d6e-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="68d6e-116">Diese Protokolldatei speichert einen Datensatz der Konvertierung von MTS-Paketen in com+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="68d6e-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="68d6e-117">Wenn während des Konvertierungs Vorgangs Fehler aufgetreten sind, ist es immer ratsam, die Protokolldatei zu überprüfen, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68d6e-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="68d6e-118">Die Protokolldatei fängt häufige Probleme, z. b. ungültige Benutzer oder Kennwort, ab.</span><span class="sxs-lookup"><span data-stu-id="68d6e-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68d6e-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68d6e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d6e-120">Ergebnisse und Probleme bei der com+-Konvertierung</span><span class="sxs-lookup"><span data-stu-id="68d6e-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="68d6e-121">Manuelle Konvertierung von MTS</span><span class="sxs-lookup"><span data-stu-id="68d6e-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="68d6e-122">MTS-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68d6e-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



