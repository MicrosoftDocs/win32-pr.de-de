---
description: Die Windows Imaging Component (WIC) ist eine erweiterbare Plattform für die digitale Abbild Erstellung unter den Betriebssystemen Windows Vista und Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Einführung (Schreiben eines WIC-Enabled Codecs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353509"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="3cefa-103">Einführung (Schreiben eines WIC-Enabled Codecs)</span><span class="sxs-lookup"><span data-stu-id="3cefa-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="3cefa-104">Die Windows Imaging Component (WIC) ist eine erweiterbare Plattform für die digitale Abbild Erstellung unter den Betriebssystemen Windows Vista und Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3cefa-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="3cefa-105">WIC ist auch unter Windows XP und Windows Server 2003 verfügbar, entweder als Teil von Microsoft .NET Framework 3,0 oder als separate Komponente, die Sie weiterverteilen können.</span><span class="sxs-lookup"><span data-stu-id="3cefa-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="3cefa-106">Jede Anwendung, die WIC verwendet, kann auf Bilder in jedem Bildformat zugreifen, Sie anzeigen, verarbeiten und drucken, das einen WIC-fähigen Codec bereitstellt. dabei wird ein einzelner Satz konsistentischer Schnittstellen verwendet, die die Notwendigkeit spezieller Kenntnisse bestimmter Formate ausschließen.</span><span class="sxs-lookup"><span data-stu-id="3cefa-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="3cefa-107">Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery und Windows 7 Photo Viewer basieren auf WIC.</span><span class="sxs-lookup"><span data-stu-id="3cefa-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="3cefa-108">Nachdem ein WIC-fähiger Codec auf einem Windows Vista-oder Windows 7-System installiert wurde, bietet das Betriebssystem das gleiche Maß an Unterstützung für das zugehörige Bildformat wie für die Standard Abbild Formate, die mit der Plattform ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="3cefa-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="3cefa-109">Da Sie den Codec für Ihr eigenes Bildformat schreiben, können Sie immer dann eine konsistente Qualität sicherstellen, wenn Ihr Bildformat verwendet wird, und Sie profitieren von den Vorteilen der vollständigen Platt Form Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="3cefa-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cefa-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cefa-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3cefa-111">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3cefa-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3cefa-112">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="3cefa-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="3cefa-113">Funktionsweise der Windows-Abbild Erstellungs Komponente</span><span class="sxs-lookup"><span data-stu-id="3cefa-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="3cefa-114">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="3cefa-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="3cefa-115">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="3cefa-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



