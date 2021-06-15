---
title: HelpContextID-Eigenschaft (Commands Collection-Objekt)
description: Erfahren Sie mehr über die HelpContextID-Eigenschaft des Commands Collection-Objekts. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ed6ccf40545e15b3603ce5abe80ef94ff4272a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068236"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="fcdb7-104">HelpContextID-Eigenschaft (Commands Collection-Objekt)</span><span class="sxs-lookup"><span data-stu-id="fcdb7-104">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="fcdb7-105">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fcdb7-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fcdb7-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fcdb7-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fcdb7-107">Gibt eine zugeordnete Kontextnummer für das Commands-Objekt zurück oder [**legt**](/windows/desktop/lwef/the-commands-collection-object) diese fest.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-107">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="fcdb7-108">Wird verwendet, um kontextsensitive Hilfe für das **Commands-Objekt** zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-108">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="fcdb7-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="fcdb7-109"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fcdb7-110">*agent.\***Characters("**_CharacterID_*_"). Commands("_*_name_*_"). HelpContextID-Nummer_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="fcdb7-110">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="fcdb7-111">Teil</span><span class="sxs-lookup"><span data-stu-id="fcdb7-111">Part</span></span>     | <span data-ttu-id="fcdb7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcdb7-112">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="fcdb7-113">*Number*</span><span class="sxs-lookup"><span data-stu-id="fcdb7-113">*Number*</span></span> | <span data-ttu-id="fcdb7-114">Eine ganze Zahl, die eine gültige Kontextnummer angibt.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-114">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcdb7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcdb7-115">Remarks</span></span>

<span data-ttu-id="fcdb7-116">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben, ruft der -Agent die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) auswählt.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-116">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="fcdb7-117">Wenn Sie eine Kontextnummer in **helpContextID** festlegen, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch diese Kontextnummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-117">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="fcdb7-118">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="fcdb7-119">Zum Erstellen einer Hilfedatei ist der Microsoft Windows-Hilfecompiler erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fcdb7-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="fcdb7-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fcdb7-120">See Also</span></span>

[<span data-ttu-id="fcdb7-121">**HelpFile-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="fcdb7-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
