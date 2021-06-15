---
title: HelpContextID-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Command-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c3c0ff5a6722dd6740c7df7e89bf2b9520053
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068511"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="e718d-104">HelpContextID-Eigenschaft (Befehlsobjekt)</span><span class="sxs-lookup"><span data-stu-id="e718d-104">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="e718d-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e718d-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e718d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e718d-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e718d-107">Gibt eine zugeordnete Kontextnummer für das Command-Objekt zurück [**oder legt diese**](/windows/desktop/lwef/the-command-object) fest.</span><span class="sxs-lookup"><span data-stu-id="e718d-107">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="e718d-108">Wird verwendet, um kontextsensitive Hilfe für das **Command-Objekt** zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="e718d-108">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="e718d-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e718d-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e718d-110">*agent.\***Characters("**_CharacterID_*_"). Commands(""). HelpContextID-Nummer_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="e718d-110">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="e718d-111">Teil</span><span class="sxs-lookup"><span data-stu-id="e718d-111">Part</span></span>     | <span data-ttu-id="e718d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e718d-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="e718d-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="e718d-113">*Number*</span></span> | <span data-ttu-id="e718d-114">Eine ganze Zahl, die eine gültige Kontextnummer angibt.</span><span class="sxs-lookup"><span data-stu-id="e718d-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e718d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e718d-115">Remarks</span></span>

<span data-ttu-id="e718d-116">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens auf die Datei festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf True festgelegt ist und der Benutzer den Befehl auswählt. </span><span class="sxs-lookup"><span data-stu-id="e718d-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="e718d-117">Wenn Sie eine Kontextnummer in [**helpContextID**](helpcontextid-property.md)festlegen, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e718d-117">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e718d-118">Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="e718d-118">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="e718d-119">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="e718d-119">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="e718d-120">Zum Erstellen einer Hilfedatei ist der Microsoft Windows-Hilfecompiler erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e718d-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e718d-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e718d-121">See Also</span></span>

[<span data-ttu-id="e718d-122">**HelpFile-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="e718d-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 
