---
title: Referenz zum Windows Media Player-Objektmodell
description: Referenz zum Windows Media Player-Objektmodell
ms.assetid: af313b94-230b-47d7-a3ad-7e23b669886f
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player Mobile, Objektmodell
- Windows Media Player-Objektmodell, Referenz
- Objektmodell, Referenz
- ActiveX-Steuerelement, Referenz
- Windows Media Player ActiveX-Steuerelement, Referenz
- Windows Media Player Mobile ActiveX-Steuerelement, Referenz
- Referenz für Objektmodell, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6128ff3f69968ddf4f8a35955907a18876ef090
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037486"
---
# <a name="windows-media-player-object-model-reference"></a><span data-ttu-id="789d6-111">Referenz zum Windows Media Player-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="789d6-111">Windows Media Player Object Model Reference</span></span>

<span data-ttu-id="789d6-112">Die Windows Media Player-Objektmodell-Referenz Abschnitte enthalten ausführliche Informationen zum Windows Media Player ActiveX-Steuerelement-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="789d6-112">The Windows Media Player Object Model Reference sections contain detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="789d6-113">Das-Objektmodell stellt Schnittstellen bereit, mit denen Entwickler Webseiten, C++-Programmen und .NET-Anwendungen Funktionen für Windows Media Player hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="789d6-113">The object model provides interfaces that let developers add Windows Media Player functionality to webpages, C++ programs, and .NET applications.</span></span>

<span data-ttu-id="789d6-114">Die Objektmodell Referenz für die Skripterstellung wird in einem Format dargestellt, das für die Verwendung mit Skriptsprachen wie Microsoft JScript konzipiert ist, und das Objektmodell wird in Bezug auf Objekte mit den zugehörigen Eigenschaften, Methoden und Ereignissen dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="789d6-114">The Object Model Reference for Scripting is presented in a style designed for use with script languages like Microsoft JScript, and it documents the object model in terms of objects with their associated properties, methods, and events.</span></span>

<span data-ttu-id="789d6-115">Die Objektmodell Referenz für C++ bietet eine Dokumentation für COM-Schnittstellen, die C++-Programmierer verwenden können, um mit dem Windows Media Player ActiveX-Steuerelement oder dem Windows Media Player Mobile ActiveX-Steuerelement zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="789d6-115">The Object Model Reference for C++ provides documentation for COM interfaces that C++ programmers can use to communicate with the Windows Media Player ActiveX control or the Windows Media Player Mobile ActiveX control.</span></span> <span data-ttu-id="789d6-116">Die meisten dieser Schnittstellen werden von der Windows Media Player-Steuerung implementiert und von der C++-Anwendung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="789d6-116">Most of these interfaces are implemented by Windows Media Player control and called by the C++ application.</span></span> <span data-ttu-id="789d6-117">Einige der Schnittstellen (z. b. **iwmpevents** und **iwmpremotemediaservices**) werden jedoch von der C++-Anwendung implementiert und vom Windows Media Player-Steuerelement aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="789d6-117">However, some of the interfaces (for example, **IWMPEvents** and **IWMPRemoteMediaServices**) are implemented by the C++ application and called by the Windows Media Player control.</span></span>

<span data-ttu-id="789d6-118">Die Objektmodell Referenz für Visual Basic .net und c# enthält Dokumentation für die Eigenschaften, Methoden und Ereignisse des **AxWindowsMediaPlayer** -Objekts sowie für Schnittstellen zum Windows Media Player ActiveX-Steuerelement, das über die COM-Interoperabilität in einer in Visual Studio .NET 2002 oder höher codierten Lösung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="789d6-118">The Object Model Reference for Visual Basic .NET and C# provides documentation for the properties, methods, and events of the **AxWindowsMediaPlayer** object and for interfaces to the Windows Media Player ActiveX control that are available through COM interoperability in a solution coded in Visual Studio .NET 2002 or later.</span></span>

<span data-ttu-id="789d6-119">Die Windows Media Player-Objektmodell Referenz enthält die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="789d6-119">The Windows Media Player Object Model Reference contains the following sections.</span></span>



| <span data-ttu-id="789d6-120">`Section`</span><span class="sxs-lookup"><span data-stu-id="789d6-120">Section</span></span>                                                                                                        | <span data-ttu-id="789d6-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="789d6-121">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="789d6-122">Objektmodell Referenz für die Skripterstellung</span><span class="sxs-lookup"><span data-stu-id="789d6-122">Object Model Reference for Scripting</span></span>](object-model-reference-for-scripting.md)                               | <span data-ttu-id="789d6-123">Enthält eine Referenz Dokumentation für die Eigenschaften, Methoden und Ereignisse, die das Objektmodell für Skriptsprachen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="789d6-123">Provides reference documentation for the properties, methods, and events that the object model makes available to scripting languages.</span></span> <span data-ttu-id="789d6-124">Diese Informationen sind auch für Visual Basic 6,0-Programmierung nützlich.</span><span class="sxs-lookup"><span data-stu-id="789d6-124">This information is also useful for Visual Basic 6.0 programming.</span></span> |
| [<span data-ttu-id="789d6-125">Objektmodell Referenz für C++</span><span class="sxs-lookup"><span data-stu-id="789d6-125">Object Model Reference for C++</span></span>](object-model-reference-for-c.md)                                             | <span data-ttu-id="789d6-126">Enthält eine Referenz Dokumentation für C++-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="789d6-126">Provides reference documentation for C++ interfaces.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="789d6-127">Objektmodell Referenz für Visual Basic .net und C #</span><span class="sxs-lookup"><span data-stu-id="789d6-127">Object Model Reference for Visual Basic .NET and C#</span></span>](object-model-reference-for-visual-basic--net-and-c.md) | <span data-ttu-id="789d6-128">Bietet eine Referenz Dokumentation für Objekte und Schnittstellen, die für Visual Basic .net-und c#-Programmierern über COM-Interoperabilität verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="789d6-128">Provides reference documentation for objects and interfaces available to Visual Basic .NET and C# programmers through COM interoperability.</span></span>                                                             |
| [<span data-ttu-id="789d6-129">Attribut Verweis</span><span class="sxs-lookup"><span data-stu-id="789d6-129">Attribute Reference</span></span>](attribute-reference.md)                                                                 | <span data-ttu-id="789d6-130">Enthält eine Referenz Dokumentation für Metadatenattribute, die für Entwickler von Windows Media Player SDK von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="789d6-130">Provides reference documentation for metadata attributes that are of interest to Windows Media Player SDK developers.</span></span>                                                                                    |
| [<span data-ttu-id="789d6-131">Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="789d6-131">Enumeration Types</span></span>](enumeration-types.md)                                                                     | <span data-ttu-id="789d6-132">Enthält eine Referenz Dokumentation für die Enumerationstypen, die von den C++-und .NET-Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="789d6-132">Provides reference documentation for the enumeration types that are used by the C++ and .NET interfaces.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="789d6-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="789d6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="789d6-134">**Windows Media Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="789d6-134">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




