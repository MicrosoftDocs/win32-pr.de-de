---
title: Sicherheitsfunktionen
description: Die Sicherheitsfunktionen für die Netzwerkverwaltung erhalten und legen Sicherheits Deskriptoren für Domänen basierte und eigenständige DFS-Stämme fest.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483846"
---
# <a name="security-functions"></a><span data-ttu-id="5b1b1-103">Sicherheitsfunktionen</span><span class="sxs-lookup"><span data-stu-id="5b1b1-103">Security Functions</span></span>

<span data-ttu-id="5b1b1-104">Die Sicherheitsfunktionen für die Netzwerkverwaltung erhalten und legen Sicherheits Deskriptoren für Domänen basierte und eigenständige DFS-Stämme fest.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="5b1b1-105">Die DFS-Sicherheitsfunktionen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="5b1b1-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="5b1b1-106">Function</span></span>                                                               | <span data-ttu-id="5b1b1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b1b1-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b1b1-108">**Netdfsgetsecurity**</span><span class="sxs-lookup"><span data-stu-id="5b1b1-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="5b1b1-109">Ruft die Sicherheits Beschreibung für das Stamm Objekt des angegebenen DFS-Stamms ab.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="5b1b1-110">**Netdfssetsecurity**</span><span class="sxs-lookup"><span data-stu-id="5b1b1-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="5b1b1-111">Sucht das Stamm Objekt für den angegebenen DFS-Stamm und legt den angegebenen Sicherheits Deskriptor darauf fest.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="5b1b1-112">**Netdfsgetstdcontainersecurity**</span><span class="sxs-lookup"><span data-stu-id="5b1b1-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="5b1b1-113">Ruft die Sicherheits Beschreibung für das Container Objekt des angegebenen eigenständigen DFS-Stamms ab.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="5b1b1-114">**Netdfssetstdcontainersecurity**</span><span class="sxs-lookup"><span data-stu-id="5b1b1-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="5b1b1-115">Sucht das Container Objekt für das angegebene eigenständige DFS-Stammverzeichnis und legt die angegebene Sicherheits Beschreibung darauf fest.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="5b1b1-116">**Netdfsgetftcontainersecurity**</span><span class="sxs-lookup"><span data-stu-id="5b1b1-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="5b1b1-117">Ruft die Sicherheits Beschreibung für das Container Objekt des angegebenen DFS-Domänen Stamms ab.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="5b1b1-118">**Netdfssetftcontainersecurity**</span><span class="sxs-lookup"><span data-stu-id="5b1b1-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="5b1b1-119">Sucht das Container Objekt für den angegebenen DFS-Domänen Stamm und legt die angegebene Sicherheits Beschreibung darauf fest.</span><span class="sxs-lookup"><span data-stu-id="5b1b1-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |
