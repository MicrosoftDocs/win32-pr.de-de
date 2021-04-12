---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicherheit (Cookbook zur Anwendungsqualität in Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218826"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="19333-103">Sicherheit (Cookbook zur Anwendungsqualität in Windows 7 und Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="19333-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="19333-104">Ab Windows Internet Explorer 7 wird Windows Internet Explorer in einem Sicherheitskontext mit dem Namen *geschützter Modus* ausgeführt, wenn Benutzer es unter dem Betriebssystem Windows Vista oder einer höheren Version ausführen.</span><span class="sxs-lookup"><span data-stu-id="19333-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="19333-105">Dieser Modus führt Internet Explorer mit einer niedrigeren Berechtigung als einer Standardbenutzer Anwendung aus, sodass bestimmte Funktionen eingeschränkt sind, insbesondere ActiveX-Steuerelemente und bestimmte Plug-in-Typen. Weitere Informationen zum geschützten Modus in Internet Explorer und dessen Auswirkungen auf die Kompatibilität finden Sie unter [Understanding and working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="19333-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="19333-106">Windows Internet Explorer 8 ermöglicht standardmäßig auch die Daten Ausführungs Verhinderung (Data Execution Prevention, DEP), mit der Anwendungen vermeiden können, beliebigen Code in Online Angriffen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="19333-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="19333-107">Einige Add-ons verwenden diese Sicherheitsfunktion jedoch möglicherweise nicht (z. b. alle Add-ons, die nicht für die Ausführung von Code verwendet werden, der sich im Arbeitsspeicher befindet, der speziell als ausführbare Datei gekennzeichnet wurde, wie z. b. Anwendungen, die mit einer älteren Version des ATL-Frameworks (ActiveX Template Library) erstellt wurden).</span><span class="sxs-lookup"><span data-stu-id="19333-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="19333-108">Internet Explorer 8 schützt Benutzer auch vor potenziellen Sicherheitsrisiken, die Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="19333-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="19333-109">Beispielsweise können Sie nicht von einer URL in einer weniger vertrauenswürdigen Zone zu einer URL in einer vertrauenswürdigeren Zone navigieren, außer durch explizite Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="19333-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="19333-110">Sie können auch bestimmte Elemente der Benutzeroberfläche des Browsers (z. b. die Adressleiste) nicht in einer nicht vertrauenswürdigen Zone (Internet) ausblenden.</span><span class="sxs-lookup"><span data-stu-id="19333-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19333-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19333-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19333-112">Entwerfen von Updates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="19333-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
