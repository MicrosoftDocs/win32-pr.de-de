---
description: Bevor eine Anwendung Daten zur Registrierung hinzufügen kann, muss Sie einen Schlüssel erstellen oder öffnen.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Öffnen, erstellen und Schließen von Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353126"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="09bcd-103">Öffnen, erstellen und Schließen von Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="09bcd-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="09bcd-104">Bevor eine Anwendung Daten zur Registrierung hinzufügen kann, muss Sie einen Schlüssel erstellen oder öffnen.</span><span class="sxs-lookup"><span data-stu-id="09bcd-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="09bcd-105">Um einen Schlüssel zu erstellen oder zu öffnen, verweist eine Anwendung immer auf den Schlüssel als Unterschlüssel eines aktuell geöffneten Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="09bcd-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="09bcd-106">Die folgenden vordefinierten Schlüssel sind immer geöffnet: **HKEY \_ local \_ Machine**, **HKEY \_ Classes \_ root**, **HKEY \_ Users** und **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="09bcd-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="09bcd-107">Eine Anwendung verwendet die [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) -Funktion, um einen Schlüssel zu öffnen, und die [**regkreatekeyex**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) -Funktion, um einen Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="09bcd-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="09bcd-108">Eine Registrierungs Struktur kann 512 Ebenen tief sein.</span><span class="sxs-lookup"><span data-stu-id="09bcd-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="09bcd-109">Sie können bis zu 32 Ebenen gleichzeitig über einen einzigen Registrierungs-API-Aufruf erstellen.</span><span class="sxs-lookup"><span data-stu-id="09bcd-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="09bcd-110">Eine Anwendung kann die [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) -Funktion verwenden, um einen Schlüssel zu schließen und die darin enthaltenen Daten in die Registrierung zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="09bcd-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="09bcd-111">**RegCloseKey** schreibt die Daten vor der Rückgabe nicht notwendigerweise in die Registrierung. Es kann bis zu mehrere Sekunden dauern, bis der Cache auf die Festplatte geleert wird.</span><span class="sxs-lookup"><span data-stu-id="09bcd-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="09bcd-112">Wenn eine Anwendung explizit Registrierungsdaten auf die Festplatte schreiben muss, kann Sie die [**regflushkey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="09bcd-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="09bcd-113">**Regflushkey** verwendet jedoch viele Systemressourcen und sollte nur aufgerufen werden, wenn dies unbedingt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="09bcd-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



