---
title: HelpContextID-Eigenschaft (Characters-Objekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Characters-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068186"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="9dbdf-104">HelpContextID-Eigenschaft (Characters-Objekt)</span><span class="sxs-lookup"><span data-stu-id="9dbdf-104">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="9dbdf-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9dbdf-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9dbdf-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9dbdf-107">Gibt eine zugeordnete Kontextnummer für das Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-107">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="9dbdf-108">Wird verwendet, um kontextsensitive Hilfe für das Zeichen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-108">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="9dbdf-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9dbdf-110">*agent.\***Characters("**_CharacterID_*_"). HelpContextID-Nummer_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="9dbdf-110">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="9dbdf-111">Teil</span><span class="sxs-lookup"><span data-stu-id="9dbdf-111">Part</span></span>     | <span data-ttu-id="9dbdf-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dbdf-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="9dbdf-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="9dbdf-113">*Number*</span></span> | <span data-ttu-id="9dbdf-114">Eine ganze Zahl, die eine gültige Kontextnummer angibt.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dbdf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dbdf-115">Remarks</span></span>

<span data-ttu-id="9dbdf-116">Um kontextorientierte Hilfe für das Zeichen zu unterstützen, weisen Sie die Kontextnummer dem Zeichen zu, das Sie beim Kompilieren der Hilfedatei für das zugehörige Hilfethema verwenden.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-116">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="9dbdf-117">Diese Eigenschaft gilt nur für den Client des Zeichens. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen des Clients aus.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-117">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="9dbdf-118">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer auf das Zeichen klickt.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-118">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="9dbdf-119">Wenn die [**HelpContextID**](helpcontextid-property.md)eine Kontextnummer enthält, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-119">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="9dbdf-120">Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-120">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="9dbdf-121">Zum Erstellen einer Hilfedatei ist der Microsoft Windows-Hilfecompiler erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9dbdf-121">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="9dbdf-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9dbdf-122">See Also</span></span>

[<span data-ttu-id="9dbdf-123">**HelpFile-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-123">**HelpFile property**</span></span>](helpfile-property.md)


 

 




