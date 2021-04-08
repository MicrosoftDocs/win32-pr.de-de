---
description: PropertyKeys und GUIDs auf tragbaren Windows-Geräten
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PropertyKeys und GUIDs auf tragbaren Windows-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866507"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="8a9fb-103">PropertyKeys und GUIDs auf tragbaren Windows-Geräten</span><span class="sxs-lookup"><span data-stu-id="8a9fb-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="8a9fb-104">Eine Eigenschaft oder ein Befehl wird durch eine PropertyKey-Struktur identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8a9fb-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="8a9fb-105">Eine PropertyKey-Struktur besteht aus zwei Teilen: einer GUID (dem fmtid-Member) und einem DWORD (dem PID-Member).</span><span class="sxs-lookup"><span data-stu-id="8a9fb-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="8a9fb-106">Der GUID-Teil wird verwendet, um die Kategorie anzugeben, zu der die Eigenschaft oder der Befehl gehört (d. h. verknüpfte Eigenschaften gehören derselben Kategorie, und zugehörige Befehle gehören derselben Kategorie an. Deshalb haben Sie dieselbe fmtid).</span><span class="sxs-lookup"><span data-stu-id="8a9fb-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="8a9fb-107">Der DWORD-Teil gibt die Eigenschaft oder Befehls-ID an und wird verwendet, um die einzelnen Eigenschaften oder Befehle innerhalb einer Eigenschaft oder Befehls Kategorie zu unterscheiden (d. h., die PID-Werte für Eigenschaften oder Befehle in derselben Kategorie werden unterschiedlich sein).</span><span class="sxs-lookup"><span data-stu-id="8a9fb-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="8a9fb-108">Der Referenz Abschnitt dieses Dokuments beschreibt alle PropertyKey-Werte, die von WPD definiert werden. Diese Werte entsprechen Befehlen, Eigenschaften und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8a9fb-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="8a9fb-109">Wenn Sie einen benutzerdefinierten PropertyKey-Wert erstellen, sollten Sie eine neue **GUID** -Kategorie definieren. Verwenden Sie die WPD- **GUID** -Werte nicht, oder Sie riskieren einen Konflikt mit vorhandenen und zukünftigen WPD-spezifischen PropertyKeys.</span><span class="sxs-lookup"><span data-stu-id="8a9fb-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a9fb-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a9fb-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a9fb-111">**Anwendungs Übersicht**</span><span class="sxs-lookup"><span data-stu-id="8a9fb-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="8a9fb-112">**Befehle**</span><span class="sxs-lookup"><span data-stu-id="8a9fb-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="8a9fb-113">**Objekt Format-GUIDs**</span><span class="sxs-lookup"><span data-stu-id="8a9fb-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="8a9fb-114">**Eigenschaften und Attribute**</span><span class="sxs-lookup"><span data-stu-id="8a9fb-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a9fb-115">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="8a9fb-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



