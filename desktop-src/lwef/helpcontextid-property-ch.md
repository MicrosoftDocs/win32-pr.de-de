---
title: HelpContextID-Eigenschaft (Character-Objekt)
description: HelpContextID (Eigenschaft)
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391396"
---
# <a name="helpcontextid-property-characters-object"></a><span data-ttu-id="c8c15-103">HelpContextID-Eigenschaft (Character-Objekt)</span><span class="sxs-lookup"><span data-stu-id="c8c15-103">HelpContextID Property (Characters Object)</span></span>

<span data-ttu-id="c8c15-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="c8c15-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c8c15-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8c15-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c8c15-106">Gibt eine zugeordnete Kontext Nummer für das Zeichen zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c8c15-106">Returns or sets an associated context number for the character.</span></span> <span data-ttu-id="c8c15-107">Wird verwendet, um die kontextbezogene Hilfe für das Zeichen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8c15-107">Used to provide context-sensitive Help for the character.</span></span>

</dd> <dt>

<span data-ttu-id="c8c15-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c8c15-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c8c15-109">\*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). HelpContextID_- \*  \[  =  *Nummer*\]</span><span class="sxs-lookup"><span data-stu-id="c8c15-109">*agent.\***Characters("**_CharacterID_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="c8c15-110">Teil</span><span class="sxs-lookup"><span data-stu-id="c8c15-110">Part</span></span>     | <span data-ttu-id="c8c15-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8c15-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="c8c15-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="c8c15-112">*Number*</span></span> | <span data-ttu-id="c8c15-113">Eine ganze Zahl, die eine gültige Kontext Nummer angibt.</span><span class="sxs-lookup"><span data-stu-id="c8c15-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8c15-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8c15-114">Remarks</span></span>

<span data-ttu-id="c8c15-115">Um die kontextabhängige Hilfe für das Zeichen zu unterstützen, weisen Sie die Kontext Nummer dem Zeichen zu, das Sie für das zugehörige Hilfethema verwenden, wenn Sie die Hilfedatei kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c8c15-115">To support context-sensitive Help for the character, assign the context number to the character you use for the associated Help topic when you compile your Help file.</span></span> <span data-ttu-id="c8c15-116">Diese Eigenschaft gilt nur für den Client des Zeichens; die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen des Clients aus.</span><span class="sxs-lookup"><span data-stu-id="c8c15-116">This property applies only to the client of the character; the setting does not affect other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="c8c15-117">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer auf das Zeichen klickt.</span><span class="sxs-lookup"><span data-stu-id="c8c15-117">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character.</span></span> <span data-ttu-id="c8c15-118">Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c8c15-118">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="c8c15-119">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c8c15-119">The current context number is the value of **HelpContextID** for the character.</span></span>

> [!Note]  
> <span data-ttu-id="c8c15-120">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="c8c15-120">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c8c15-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8c15-121">See Also</span></span>

[<span data-ttu-id="c8c15-122">**HelpFile (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="c8c15-122">**HelpFile property**</span></span>](helpfile-property.md)


 

 




