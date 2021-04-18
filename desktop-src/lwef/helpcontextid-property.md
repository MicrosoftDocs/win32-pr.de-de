---
title: HelpContextID-Eigenschaft (Commands-Auflistungs Objekt)
description: HelpContextID (Eigenschaft)
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474922"
---
# <a name="helpcontextid-property-commands-collection-object"></a><span data-ttu-id="94ed2-103">HelpContextID-Eigenschaft (Commands-Auflistungs Objekt)</span><span class="sxs-lookup"><span data-stu-id="94ed2-103">HelpContextID Property (Commands Collection Object)</span></span>

<span data-ttu-id="94ed2-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="94ed2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="94ed2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="94ed2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="94ed2-106">Gibt eine zugeordnete Kontext Nummer für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="94ed2-106">Returns or sets an associated context number for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="94ed2-107">Wird verwendet, um kontextbezogene Hilfe für das **Commands** -Objekt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="94ed2-107">Used to provide context-sensitive Help for the **Commands** object.</span></span>

</dd> <dt>

<span data-ttu-id="94ed2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="94ed2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="94ed2-109">*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_\*_"). HelpContextID_- \*  \[  =  *Nummer*\]</span><span class="sxs-lookup"><span data-stu-id="94ed2-109">*agent.\***Characters("**_CharacterID_*_").Commands("_*_name_*_").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="94ed2-110">Teil</span><span class="sxs-lookup"><span data-stu-id="94ed2-110">Part</span></span>     | <span data-ttu-id="94ed2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94ed2-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="94ed2-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="94ed2-112">*Number*</span></span> | <span data-ttu-id="94ed2-113">Eine ganze Zahl, die eine gültige Kontext Nummer angibt.</span><span class="sxs-lookup"><span data-stu-id="94ed2-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94ed2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94ed2-114">Remarks</span></span>

<span data-ttu-id="94ed2-115">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt auswählt.</span><span class="sxs-lookup"><span data-stu-id="94ed2-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span> <span data-ttu-id="94ed2-116">Wenn Sie in **HelpContextID** eine Kontext Nummer festlegen, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch diese Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="94ed2-116">If you set a context number in the **HelpContextID**, Agent calls Help and searches for the topic identified by that context number.</span></span>

<span data-ttu-id="94ed2-117">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="94ed2-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="94ed2-118">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="94ed2-118">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="94ed2-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="94ed2-119">See Also</span></span>

[<span data-ttu-id="94ed2-120">**HelpFile (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94ed2-120">**HelpFile property**</span></span>](helpfile-property.md)


 

 
