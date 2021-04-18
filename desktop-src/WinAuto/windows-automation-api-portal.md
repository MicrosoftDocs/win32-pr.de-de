---
title: Übersicht über die Windows Automation-API
description: Microsoft Windows bietet zwei API-Spezifikationen für die Benutzeroberflächen-Barrierefreiheit und Softwaretest Automatisierung Microsoft Active Accessibility und Microsoft UI Automation.
ms.assetid: 73acc580-9573-40ea-8727-b0e7292b2a4c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac67c5311d0d936e45235c527ebb15c238ba808
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315657"
---
# <a name="windows-accessibility-api-overview"></a><span data-ttu-id="6dfa6-103">Übersicht über die Barrierefreiheit von Windows</span><span class="sxs-lookup"><span data-stu-id="6dfa6-103">Windows Accessibility API overview</span></span>

<span data-ttu-id="6dfa6-104">Dieser Abschnitt enthält allgemeine Übersichten und eine ausführliche API-Referenz für die Microsoft Windows Automation-API 3,0, die die Windows-Implementierung der Microsoft [UI Automation Specification](./uiauto-specandcommunitypromise.md)und Microsoft Active Accessibility (Legacy-Feature, das in Windows 95 als Plattform-Add-in eingeführt wurde) enthält.</span><span class="sxs-lookup"><span data-stu-id="6dfa6-104">This section provides high-level overviews and detailed API reference for both the Microsoft Windows Automation API 3.0, which includes the Windows implementation of the Microsoft [UI Automation Specification](./uiauto-specandcommunitypromise.md), and Microsoft Active Accessibility (legacy feature introduced in Windows 95 as a platform add-in).</span></span>

<span data-ttu-id="6dfa6-105">Wir beschreiben die Ähnlichkeiten und Unterschiede zwischen Microsoft Active Accessibility und der Benutzeroberflächen Automatisierung, den Komponenten und Features, die die Zusammenarbeit der beiden Technologien ermöglichen, und bieten Richtlinien für die Auswahl der Technologie, die für Ihr spezielles Szenario implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dfa6-105">We describe the similarities and differences between Microsoft Active Accessibility and UI Automation, the components and features that enable the two technologies to work together, and provide guidelines for choosing which technology to implement for your specific scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dfa6-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dfa6-106">Related topics</span></span>

[<span data-ttu-id="6dfa6-107">Benutzeroberflächenautomatisierungs-Community Promise</span><span class="sxs-lookup"><span data-stu-id="6dfa6-107">UI Automation Community Promise</span></span>](./uiauto-specandcommunitypromise.md)