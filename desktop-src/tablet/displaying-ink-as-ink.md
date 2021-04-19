---
description: Das Standardverhalten für das InkEdit-Steuerelement besteht darin, frei Hand Eingaben zu erkennen und in Text zu konvertieren, nachdem ein kurzes Timeout abgelaufen ist.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Anzeigen von frei Hand Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349627"
---
# <a name="displaying-ink-as-ink"></a><span data-ttu-id="0f54d-103">Anzeigen von frei Hand Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f54d-103">Displaying Ink as Ink</span></span>

<span data-ttu-id="0f54d-104">Das Standardverhalten für das [InkEdit](inkedit-control-reference.md) -Steuerelement besteht darin, frei Hand Eingaben zu erkennen und in Text zu konvertieren, nachdem ein kurzes Timeout abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="0f54d-104">The default behavior for the [InkEdit](inkedit-control-reference.md) control is to recognize and convert ink into text after a brief timeout has expired.</span></span> <span data-ttu-id="0f54d-105">Da es sich bei dem Steuerelement um eine übergeordnete Klasse von [RichEdit](../controls/rich-edit-controls.md)handelt, ist es auch möglich, frei Hand Eingaben im Steuerelement einzubetten und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0f54d-105">Because the control is a superclass of [RichEdit](../controls/rich-edit-controls.md), it is also possible to embed and display ink within the control.</span></span> <span data-ttu-id="0f54d-106">Jedes Wort wird als [**InkDisp**](inkdisp-class.md) -Objekt in das-Steuerelement eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0f54d-106">Each word is inserted into the control as an [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="0f54d-107">Das **InkDisp** -Objekt enthält die frei Hand Eingaben und deren Erkennungs Alternativen.</span><span class="sxs-lookup"><span data-stu-id="0f54d-107">The **InkDisp** object contains the ink and its recognition alternates.</span></span>

<span data-ttu-id="0f54d-108">Beim Einfügen wird die frei Hand Eingabe auf den aktuellen Schrift Grad skaliert, und andere Umgebungs Eigenschaften, z. b. kursiv oder Fett, werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="0f54d-108">When inserted, the ink is scaled to the current font size and other ambient properties, such as italics or bold, are applied.</span></span> <span data-ttu-id="0f54d-109">Wenn der Benutzer den Text eines [**InkDisp**](inkdisp-class.md) -Objekts bearbeitet, muss er zuerst die frei Hand Eingaben in Text konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0f54d-109">If the user chooses to edit the text of an [**InkDisp**](inkdisp-class.md) object, he or she must first convert the ink to text.</span></span>

> [!Note]  
> <span data-ttu-id="0f54d-110">Alle alternativen Freihand-und Erkennungs Daten gehen während der Konvertierung verloren.</span><span class="sxs-lookup"><span data-stu-id="0f54d-110">All ink and recognition alternate data is lost during the conversion.</span></span>

 

<span data-ttu-id="0f54d-111">Diese Funktion ist nur auf Computern verfügbar, auf denen Microsoft Windows XP Tablet PC Edition, Windows Vista oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f54d-111">This feature is available only on computers that run Microsoft Windows XP Tablet PC Edition, Windows Vista, or later.</span></span>

 

 
