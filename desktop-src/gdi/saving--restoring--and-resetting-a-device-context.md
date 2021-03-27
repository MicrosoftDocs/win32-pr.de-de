---
description: 'Mit den folgenden Funktionen kann eine Anwendung einen Gerätekontext speichern, wiederherstellen und zurücksetzen: savedc, restoredc und ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Speichern, wiederherstellen und Zurücksetzen eines Geräte Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979792"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="1c758-103">Speichern, wiederherstellen und Zurücksetzen eines Geräte Kontexts</span><span class="sxs-lookup"><span data-stu-id="1c758-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="1c758-104">Mit den folgenden Funktionen kann eine Anwendung einen Gerätekontext speichern, wiederherstellen und zurücksetzen: [**savedc**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**restoredc**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)und [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span><span class="sxs-lookup"><span data-stu-id="1c758-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="1c758-105">Die savedc-Funktion zeichnet in einem speziellen GDI-Stapel die Grafik Objekte des aktuellen Domänen Controllers und deren Attribute und Grafikmodi auf.</span><span class="sxs-lookup"><span data-stu-id="1c758-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="1c758-106">Eine Zeichnungsanwendung kann diese Funktion aufzurufen, bevor ein Benutzer mit der Zeichnung beginnt, den ursprünglichen Zustand der Anwendung zu speichern und einen sauberen Slate für den Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1c758-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="1c758-107">Um in diesen ursprünglichen Zustand zurückzukehren, ruft die Anwendung die restoredc-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1c758-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="1c758-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) wird zum Zurücksetzen von Drucker-DC-Daten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1c758-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="1c758-109">Eine Anwendung ruft diese Funktion auf, um die Papier Ausrichtung, die Papiergröße, den Ausgabe Skalierungsfaktor, die Anzahl der zu druckenden Kopien, die Papier Quelle (oder den bin), den Duplex Modus usw. zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1c758-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="1c758-110">In der Regel Ruft eine Anwendung diese Funktion auf, nachdem ein Benutzer eine der Druckeroptionen geändert hat und das System eine [**WM \_ devmodechange**](wm-devmodechange.md) -Meldung ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1c758-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 



