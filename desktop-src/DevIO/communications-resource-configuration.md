---
description: Die CommConfig-Struktur definiert die Konfiguration einer Kommunikations Ressource, seriell oder anderweitig.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Kommunikationsressourcen Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126800"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="d7ecd-103">Kommunikationsressourcen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ecd-103">Communications Resource Configuration</span></span>

<span data-ttu-id="d7ecd-104">Die [**CommConfig**](/windows/desktop/api/Winbase/ns-winbase-commconfig) -Struktur definiert die Konfiguration einer Kommunikations Ressource, seriell oder anderweitig.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="d7ecd-105">Das Format der Struktur variiert abhängig vom Typ der Kommunikations Ressource (Anbieter Untertyp).</span><span class="sxs-lookup"><span data-stu-id="d7ecd-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="d7ecd-106">Die ersten Strukturmember sind von allen Kommunikationsressourcen gemeinsam. für bestimmte Anbieter Untertypen werden zusätzliche Member definiert.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="d7ecd-107">Bestimmte Dienstanbieter können auch die **CommConfig** -Struktur erweitern.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="d7ecd-108">Eine Anwendung kann die Konfiguration einer Kommunikations Ressource mithilfe der Funktionen [**getcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) und [**setcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="d7ecd-109">Beim Öffnen wird eine Kommunikations Ressource mit der Standardkonfiguration für den Anbieter Untertyp initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="d7ecd-110">Um die Standardkonfiguration für einen Anbieter Untertyp abzurufen und festzulegen, verwenden Sie die Funktionen [**getdefaultcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) und [**setdefaultcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .</span><span class="sxs-lookup"><span data-stu-id="d7ecd-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="d7ecd-111">Um den Benutzer zur Eingabe von Konfigurationsinformationen aufzufordern, verwenden Sie die [**commconfigdialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="d7ecd-112">Diese Funktion zeigt ein vom Dienstanbieter definiertes Dialogfeld an und füllt eine [**CommConfig**](/windows/desktop/api/Winbase/ns-winbase-commconfig) -Struktur auf Grundlage von Benutzereingaben aus.</span><span class="sxs-lookup"><span data-stu-id="d7ecd-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



